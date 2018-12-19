---
title: Plugin Config
page_title: Plugin Config | JustDecompile Documentation
description: Documentation page about Plugin Config.
previous_url: /plugin-basics-plugin-config.html
slug: plugin-config
published: True
position: 2
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


<div id="syntaxCodeBlocks" class="code"><span><table><tr><th>XML</th></tr><tr><td><pre xml:space="preserve"><span class="highlight-xml-bracket">&lt;</span><span class="highlight-xml-tag">Licenses</span><span class="highlight-xml-bracket">&gt;</span>
<span class="highlight-xml-bracket">&lt;</span><span class="highlight-xml-tag">License</span> <span class="highlight-xml-attribute-name">Title</span><span class="highlight-xml-attribute-equal">=</span><span class="highlight-xml-attribute-value">"title1"</span><span class="highlight-xml-bracket">&gt;</span>value1<span class="highlight-xml-bracket">&lt;/</span><span class="highlight-xml-tag">License</span><span class="highlight-xml-bracket">&gt;</span>
<span class="highlight-xml-bracket">&lt;</span><span class="highlight-xml-tag">License</span> <span class="highlight-xml-attribute-name">Title</span><span class="highlight-xml-attribute-equal">=</span><span class="highlight-xml-attribute-value">"title2"</span><span class="highlight-xml-bracket">&gt;</span>value2<span class="highlight-xml-bracket">&lt;/</span><span class="highlight-xml-tag">License</span><span class="highlight-xml-bracket">&gt;</span>
<span class="highlight-xml-bracket">&lt;/</span><span class="highlight-xml-tag">Licenses</span><span class="highlight-xml-bracket">&gt;</span></pre></td></tr></table></span></div>


This field is optional.

Here is an example of what a PluginConfig.xml normally looks like:


<div id="syntaxCodeBlocks" class="code"><span><table><tr><th>XML</th></tr><tr><td><pre xml:space="preserve"><span class="highlight-xml-bracket">&lt;?</span><span class="highlight-xml-tag">xml</span> <span class="highlight-xml-attribute-name">version</span><span class="highlight-xml-attribute-equal">=</span><span class="highlight-xml-attribute-value">"1.0"</span> <span class="highlight-xml-attribute-name">encoding</span><span class="highlight-xml-attribute-equal">=</span><span class="highlight-xml-attribute-value">"utf-8"</span> <span class="highlight-xml-bracket">?&gt;</span>
<span class="highlight-xml-bracket">&lt;</span><span class="highlight-xml-tag">PluginConfig</span><span class="highlight-xml-bracket">&gt;</span>
  <span class="highlight-xml-bracket">&lt;</span><span class="highlight-xml-tag">Name</span><span class="highlight-xml-bracket">&gt;</span>My JustDecompile Plugin<span class="highlight-xml-bracket">&lt;/</span><span class="highlight-xml-tag">Name</span><span class="highlight-xml-bracket">&gt;</span>
  <span class="highlight-xml-bracket">&lt;</span><span class="highlight-xml-tag">Author</span><span class="highlight-xml-bracket">&gt;</span>John Smith<span class="highlight-xml-bracket">&lt;/</span><span class="highlight-xml-tag">Author</span><span class="highlight-xml-bracket">&gt;</span>
  <span class="highlight-xml-bracket">&lt;</span><span class="highlight-xml-tag">Description</span><span class="highlight-xml-bracket">&gt;</span>
    My plugin for JustDecompile
  <span class="highlight-xml-bracket">&lt;/</span><span class="highlight-xml-tag">Description</span><span class="highlight-xml-bracket">&gt;</span>
  <span class="highlight-xml-bracket">&lt;</span><span class="highlight-xml-tag">Version</span><span class="highlight-xml-bracket">&gt;</span>2012.2.1121.0<span class="highlight-xml-bracket">&lt;/</span><span class="highlight-xml-tag">Version</span><span class="highlight-xml-bracket">&gt;</span>
  <span class="highlight-xml-bracket">&lt;</span><span class="highlight-xml-tag">SupportedJDversion</span><span class="highlight-xml-bracket">&gt;</span>2012.2.1121.0<span class="highlight-xml-bracket">&lt;/</span><span class="highlight-xml-tag">SupportedJDversion</span><span class="highlight-xml-bracket">&gt;</span>
  <span class="highlight-xml-bracket">&lt;</span><span class="highlight-xml-tag">Guid</span><span class="highlight-xml-bracket">&gt;</span>01CFD330-F85D-4ECF-8E25-2DCB6C2D4001<span class="highlight-xml-bracket">&lt;/</span><span class="highlight-xml-tag">Guid</span><span class="highlight-xml-bracket">&gt;</span>
  <span class="highlight-xml-bracket">&lt;</span><span class="highlight-xml-tag">Url</span><span class="highlight-xml-bracket">&gt;</span>https://www.telerik.com/products/decompiler/extensions.aspx#my-justdecompile-plug-in<span class="highlight-xml-bracket">&lt;/</span><span class="highlight-xml-tag">Url</span><span class="highlight-xml-bracket">&gt;</span>
  <span class="highlight-xml-bracket">&lt;</span><span class="highlight-xml-tag">Licenses</span><span class="highlight-xml-bracket">&gt;</span>
    <span class="highlight-xml-bracket">&lt;</span><span class="highlight-xml-tag">License</span> <span class="highlight-xml-attribute-name">Title</span><span class="highlight-xml-attribute-equal">=</span><span class="highlight-xml-attribute-value">"LICENSE"</span><span class="highlight-xml-bracket">&gt;</span>
      <span class="highlight-xml-bracket">&lt;![CDATA[</span><span class="highlight-xml-cdata">
        My License Conditions.
      </span><span class="highlight-xml-bracket">]]&gt;</span>
    <span class="highlight-xml-bracket">&lt;/</span><span class="highlight-xml-tag">License</span><span class="highlight-xml-bracket">&gt;</span>
  <span class="highlight-xml-bracket">&lt;/</span><span class="highlight-xml-tag">Licenses</span><span class="highlight-xml-bracket">&gt;</span>
<span class="highlight-xml-bracket">&lt;/</span><span class="highlight-xml-tag">PluginConfig</span><span class="highlight-xml-bracket">&gt;</span></pre></td></tr></table></span></div>

