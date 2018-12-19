---
title: TreeViewItemCollectionChangedEvent
page_title: TreeViewItemCollectionChangedEvent | JustDecompile Documentation
description: Documentation page about TreeViewItemCollectionChangedEvent.
previous_url: /events-treeviewitemcollectionchangedevent.html
slug: treeviewitemcollectionchangedevent
published: True
position: 5
---

# TreeViewItemCollectionChangedEvent



This class provides a push notification to all of the clients subscribers, when file(s) are loaded/removed from/to JustDecompile. Event base notification is dispatched to all of the subscribers.

## Syntax

<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve"><span class="highlight-keyword">public</span> <span class="highlight-keyword">class</span> TreeViewItemCollectionChangedEvent : CompositePresentationEvent&lt;IEnumerable&lt;ITreeViewItem&gt;&gt;
{
}

<span class="highlight-keyword">public</span> <span class="highlight-keyword">interface</span> ITreeViewItem
{
      TreeNodeType TreeNodeType { <span class="highlight-keyword">get</span>; }
}</pre></td></tr></table></span></div>

## Example

<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve"><span class="highlight-keyword">public</span> <span class="highlight-keyword">void</span> OnImportsSatisfied()
{
    <span class="highlight-keyword">this</span>.eventAggregator.GetEvent&lt;TreeViewItemCollectionChangedEvent&gt;().Subscribe(OnTreeViewItemCollectionChangedEvent);
}

<span class="highlight-keyword">private</span> <span class="highlight-keyword">void</span> LoadAssembliesIntoPlugin(IEnumerable&lt;ITreeViewItem&gt;assemblies)
{
    <span class="highlight-keyword">this</span>.assemblies = assemblies;
}</pre></td></tr></table></span></div>

A collection of [ITreeViewItem](/api/t_justdecompile_api_core_itreeviewitem) is provided by JustDecompile to all of the event subscribers. Currently the collection may contain [IAssemblyDefinitionTreeViewItem](/api/t_justdecompile_api_core_iassemblydefinitiontreeviewitem) (s) or [IXapTreeViewItem](/api/t_justdecompile_api_core_ixaptreeviewitem) (s) only.

