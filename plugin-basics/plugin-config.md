---
title: Plugin Config
page_title: Plugin Config | UI for ASP.NET AJAX Documentation
description: Plugin Config
slug: telerikjustdecompilehelp/plugin-basics/plugin-config
tags: plugin,config
published: True
position: 1
---

# Plugin Config






						Every plugin author should provide a PluginConfig.xml in order to get its plugin loaded in JustDecompile. PluginConfig.xml resides in the same folder as the plugin module.
					


						PluginConfig.xml structure:
						


							- Name: Plugin name. This will be displayed in the name column section in the Plugin Manager window. This field is required.
						


							- Author: The author name. This field is optional and can be omitted.
						


							- Description: A summary of the plugin functionality and features. Description is displayed in the download section of the Plugin Manager window. This field is required.
						


							- Guid: Unique plugin identifier. It should comply with the universally unique identifier (UUID) standard: written in text as a sequence of hexadecimal digits separated into five groups, separated by hyphens such as: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. This field is required.
						


							- Version: This field provides the actual version of the plugin (from 2 to 4 part version number - major.minor.[build].[update]). Its value should be incremented accordingly when publishing a new version of the plugin. The version is displayed in the Plugin Manager window. This field is required.
						


							- Url: The url of the plugin home page. Its value is displayed by the Plugin Manager window. This field is optional.
						


							- SupportedJDversion: The minimum supported version of JustDecompile thet the plugin supports. The plugin will not loaded in case the version specified in this field is greater than the installed version of JustDecompile. This field is required.
						


						- Licenses: This field defines all the licenses the end user has to accept in order to download and install the plugin. It is a collection of license agreements License nodes. E.g.:
						

	
							<Licenses>
							<License Title="title1">value1</License>
							<License Title="title2">value2</License>
							</Licenses>
						


						This field is optional.
					


						Here is an example of what a PluginConfig.xml normally looks like:
						

	
							<?xml version="1.0" encoding="utf-8" ?>
							<PluginConfig>
								<Name>My JustDecompile Plugin</Name>
								<Author>John Smith</Author>
								<Description>
									My plugin for JustDecompile
								</Description>
								<Version>2012.2.1121.0</Version>
								<SupportedJDversion>2012.2.1121.0</SupportedJDversion>
								<Guid>01CFD330-F85D-4ECF-8E25-2DCB6C2D4001</Guid>
								<Url>http://www.telerik.com/products/decompiler/extensions.aspx#my-justdecompile-plug-in</Url>
								<Licenses>
									<License Title="LICENSE">
										<![CDATA[
											My License Conditions.
										]]>
									</License>
								</Licenses>
							</PluginConfig>
						


