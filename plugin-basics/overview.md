---
title: Overview
page_title: Plugin Basics | JustDecompile Documentation
description: Documentation page about Plugin Basics.
previous_url: /plugin-basics.html
slug: overview
published: True
position: 0
---

# Plugin Basics



### Plugin Discoverability


*   JustDecompile will load on startup all the plugins residing in the subfolders (but not in the folder itself) of the [InstallationRoot]\Libraries\Plugins folder.

*   Each plugin should be Prism module (see [Plugin Module](plugin-module)).

*   The assembly that contains the Prism module should have the string "Module" somewhere in its name.


