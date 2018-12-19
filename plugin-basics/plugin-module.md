---
title: Plugin Module
page_title: Plugin Module | JustDecompile Documentation
description: Documentation page about Plugin Module.
previous_url: /plugin-basics-plugin-module.html
slug: plugin-module
published: True
position: 1
---

# Plugin Module



JustDecompile leverages [MEF](https://mef.codeplex.com/) and [Prism](https://compositewpf.codeplex.com/) for discovering, loading and composing any plugins and their corresponding dependencies.

A plugin is a Prism module exposed through MEF.

To be exposed as Prism module the plugin should contain a class marked with the ModuleExport attribute and implementing the IModule interface (see the example below). The Initialize() method of that class will be called as soon as JustDecompile loads the plugin in its application domain. At this point the plugin can commence executing its custom logic.

<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve">[ModuleExport(<span class="highlight-keyword">typeof</span>(PluginModule))]
<span class="highlight-keyword">public</span> <span class="highlight-keyword">class</span> PluginModule : IModule
{
    <span class="highlight-keyword">public</span> <span class="highlight-keyword">void</span> Initialize()
    {
        <span class="highlight-comment">// Put your initialization logic here.</span>
    }
}</pre></td></tr></table></span></div>
