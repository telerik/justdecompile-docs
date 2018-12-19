---
title: SelectedTreeViewItemChangedEvent
page_title: SelectedTreeViewItemChangedEvent | JustDecompile Documentation
description: Documentation page about SelectedTreeViewItemChangedEvent.
previous_url: /events-selectedtreeviewitemchangedevent.html
slug: selectedtreeviewitemchangedevent
published: True
position: 2
---

# SelectedTreeViewItemChangedEvent



This class provides a push notification to all of the clients subscribers when the selected node in JustDecompile assembly list navigation tree changes.

## Syntax

<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve"><span class="highlight-keyword">public</span> <span class="highlight-keyword">class</span> SelectedTreeViewItemChangedEvent : CompositePresentationEvent&lt;ITreeViewItem&gt;
{
}</pre></td></tr></table></span></div>

## Example


<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve"><span class="highlight-keyword">public</span> <span class="highlight-keyword">void</span> OnImportsSatisfied()
{
    <span class="highlight-keyword">this</span>.eventAggregator.GetEvent&lt;SelectedTreeViewItemChangedEvent&gt;().Subscribe(OnTreeViewItemCollectionChangedEvent);
}

<span class="highlight-keyword">private</span> <span class="highlight-keyword">void</span> OnTreeViewItemCollectionChangedEvent(ITreeViewItem selectedTreeItem)
{
    <span class="highlight-keyword">this</span>.selectedTreeItem = selectedTreeItem;
}</pre></td></tr></table></span></div>


The ITreeViewIteminstance provided by the event designates the new selected node in the assembly list navigation tree. By exploring its TreeNodeType property, you can safely cast the instance to one of the following types:

*   **[IAssemblyDefinitionTreeViewItem](/api/t_justdecompile_api_core_iassemblydefinitiontreeviewitem):** Implemented by assembly node in the assembly list navigation tree.

*   **[IAssemblyModuleDefinitionTreeViewItem](/api/t_justdecompile_api_core_iassemblymoduledefinitiontreeviewitem):** Implemented by assembly module node in the assembly list navigation tree.

*   **[IAssemblyReferenceTreeViewItem](/api/t_justdecompile_api_core_iassemblyreferencetreeviewitem):** Implemented by assembly reference node in the assembly list navigation tree.

*   **[INamespaceTreeViewItem](/api/t_justdecompile_api_core_inamespacetreeviewitem):** Implemented by namespace node in the assembly list navigation tree.

*   **[ITypeDefinitionTreeViewItem](/api/t_justdecompile_api_core_itypedefinitiontreeviewitem):** Implemented by type node in the assembly list navigation tree.

*   **[IBaseTypeDefinitionTreeViewItem](/api/t_justdecompile_api_core_ibasetypedefinitiontreeviewitem):** Implemented by base type node in the assembly list navigation tree.

*   **[IInheritTypeDefinitionTreeViewItem](/api/t_justdecompile_api_core_iinherittypedefinitiontreeviewitem):** Implemented by inherited type node in the assembly list navigation tree.

*   **[IResourceTreeViewItem](/api/t_justdecompile_api_core_iresourcetreeviewitem):** Implemented by resource node in the assembly list navigation tree.

*   **[IPropertyDefinitionTreeViewItem](/api/t_justdecompile_api_core_ipropertydefinitiontreeviewitem):** Implemented by property node in the assembly list navigation tree.

*   **[IMethodDefinitionTreeViewItem](/api/t_justdecompile_api_core_imethoddefinitiontreeviewitem):** Implemented by method node in the assembly list navigation tree.

*   **[IFieldDefinitionTreeViewItem](/api/t_justdecompile_api_core_ifielddefinitiontreeviewitem):** Implemented by field node in the assembly list navigation tree.

*   **[IEventDefinitionTreeViewItem](/api/t_justdecompile_api_core_ieventdefinitiontreeviewitem):** Implemented by event node in the assembly list navigation tree.

*   **[IXapTreeViewItem](/api/t_justdecompile_api_core_ixaptreeviewitem):** Implemented by Silverlight XAP node in the assembly list navigation tree.