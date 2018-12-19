---
title: Getting started
page_title: Getting started | JustDecompile Documentation
description: Documentation page about Getting started.
previous_url: /getting-started.html
slug: getting-started
published: True
position: 0
---

# Getting started


 **This manual provides basic guidelines for creating JustDecompile plugins and it serves as a roadmap to the developer resources and documentation.** 

*   [MEF](https://mef.codeplex.com/) and [Prism](https://compositewpf.codeplex.com/) are the only ways to communicate to JustDecompile.

    Justdecompile plugins are Prism modules. JustDecompile notifies the loaded plugins about user actions using Prism's EventAggregator service. The plugins use a set of predefined Prism regions to display any UI elements needed to interact with the user.

    JustDecompile might expose some of its functionality via MEF in the form of services.

    Thus JustDecompile is decoupled from its plugins.

*   The only JustDecompile assembly that the plugins need to refer directly is JustDecompile.API.dll. It contains a set of interfaces used by JustDecompile's events exposed by the Prism EventAggregator service mentioned above. Some of the interfaces in JustDecompile.API.dll are used by the MEF exposed services mentioned above.

    By design only interfaces and no types are to be exposed in JustDecompile's API

*   JustDecompile.API.dll strong name will change only if breaking changes are introduced. In all other cases only the file version of that assembly will change. Since that is the only assembly that a plugin will ever refer (see above) in effect that means that a plugin does not have to be recompiled against every new release of JustDecompile. A plugin has to be recompiled only if breaking changes to the API occur.
