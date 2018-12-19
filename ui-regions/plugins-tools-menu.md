---
title: Plugins Tools Menu
page_title: Plugins Tools Menu | JustDecompile Documentation
description: Documentation page about Plugins Tools Menu.
previous_url: /ui-regions-plugins-tools-menu.html
slug: plugins-tools-menu
published: True
position: 2
---

# Plugins Tools Menu



 **The UI elements placed in this region will pop up in the top level toolbar menu area.** 

The menu items residing in this region should implement the [IMenuItem](t_justdecompile_api_core_imenuitem) interface.

![Toolbar](/media/Toolbar.png)

## Example

**Code implementaion:**

<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve">[ModuleExport(<span class="highlight-keyword">typeof</span>(PluginModule))]
<span class="highlight-keyword">public</span> <span class="highlight-keyword">class</span> PluginModule : IModule, IPartImportsSatisfiedNotification
{
    <span class="highlight-keyword">public</span> <span class="highlight-keyword">void</span> OnImportsSatisfied()
    {
        <span class="highlight-keyword">this</span>.regionManager.AddToRegion(<span class="highlight-literal">"ToolMenuRegion"</span>, ToolMenuItem);
    }
}</pre></td></tr></table></span></div>

Tip |
--- |
| The plugin view model should implement [INotifyPropertyChanged](https://msdn.microsoft.com/en-us/library/system.componentmodel.inotifypropertychanged.aspx) interface, when it needs to provide dynamic property notification to the UI region where it's injected in.