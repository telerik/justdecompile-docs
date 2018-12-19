---
title: Codeviewer Plugins Area
page_title: Codeviewer Plugins Area | JustDecompile Documentation
description: Documentation page about Codeviewer Plugins Area.
previous_url: /ui-regions-codeviewer-plugins-area.html
slug: codeviewer-plugins-area
published: True
position: 3
---

# Codeviewer Plugins Area



**The UI elements placed in this region will pop up under the main code viewer area.**

![CodeViewerPluginArea](/media/CodeViewerPluginArea.png)

## Example
<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve">[ModuleExport(<span class="highlight-keyword">typeof</span>(PluginModule))]
<span class="highlight-keyword">public</span> <span class="highlight-keyword">class</span> PluginModule : IModule, IPartImportsSatisfiedNotification
{
    <span class="highlight-keyword">public</span> <span class="highlight-keyword">void</span> OnImportsSatisfied()
    {
        <span class="highlight-keyword">this</span>.regionManager.AddToRegion(<span class="highlight-literal">"PluginRegion"</span>, PluginRegionView);
    }
}</pre></td></tr></table></span></div>

