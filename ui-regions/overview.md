---
title: Overview
page_title: UI Regions | JustDecompile Documentation
description: Documentation page about UI Regions.
previous_url: /ui-regions.html
slug: overview
published: True
position: 0
---

# UI Regions



## Plugin UI Basics

A plugin can display its own UI elements at a number of predefined, named locations in Justdecompile UI. These locations are called "regions".

JustDecompile uses [Prism]() regions to implement this functionality. Regions can be accessed by a plugin through the Region Manager (IRegionManager) Prism service.


## The Region Manager Service

An instance of the Region Manager service is created by the MEF engine when application is started. Plugins can get a reference
to this instance by decorating a local variable of type IRegionManager with the Import attribute.

<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve">[Import]
<span class="highlight-keyword">private</span> IRegionManager regionManager;</pre></td></tr></table></span></div>

Note |
---|
| MEF provides an IPartImportsSatisfiedNotification interface that enables implementers to be notified when a part's imports have been satisfied. It contains a single OnImportsSatisfied() method, which is called when a part's imports have been satisfied and it is safe to use. |

<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve">[ModuleExport(<span class="highlight-keyword">typeof</span>(PluginModule))]
<span class="highlight-keyword">public</span> <span class="highlight-keyword">class</span> PluginModule : IModule, IPartImportsSatisfiedNotification
{
        <span class="highlight-keyword">public</span> <span class="highlight-keyword">void</span> OnImportsSatisfied()
        {
            <span class="highlight-keyword">this</span>.regionManager.AddToRegion(<span class="highlight-literal">"AssemblyTreeViewContextMenuRegion"</span>, assemblyNodeContextMenu);
        }
        ......
}</pre></td></tr></table></span></div>

## Regions List

* [Plugins Tools Menu](plugins-tools-menu)

* [Codeviewer Plugins Area](codeviewer-plugins-area)

* [Selected Assembly Info Area](selected-assembly-info-area)

* [Assembly Tree Context Menu](assembly-tree-context-menu)


