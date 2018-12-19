---
title: Selected Assembly Info Area
page_title: Selected Assembly Info Area | JustDecompile Documentation
description: Documentation page about Selected Assembly Info Area.
previous_url: /ui-regions-selected-assembly-info-area.html
slug: selected-assembly-info-area
published: True
position: 4
---

# Selected Assembly Info Area



 **The UI elements placed in this region will pop up in the selected assembly info area.** 

![assemblyinfo](/media/assemblyinfo.png)

## Example

**Code implementaion:**
<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve">[ModuleExport(<span class="highlight-keyword">typeof</span>(PluginModule))]
<span class="highlight-keyword">public</span> <span class="highlight-keyword">class</span> PluginModule : IModule, IPartImportsSatisfiedNotification
{
    <span class="highlight-keyword">public</span> <span class="highlight-keyword">void</span> OnImportsSatisfied()
    {
        <span class="highlight-keyword">this</span>.regionManager.AddToRegion(<span class="highlight-literal">"AssemblyInfoRegion"</span>, AssemblyInfoRegionView);
    }
}</pre></td></tr></table></span></div>

