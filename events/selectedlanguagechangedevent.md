---
title: SelectedLanguageChangedEvent
page_title: SelectedLanguageChangedEvent | UI for ASP.NET AJAX Documentation
description: SelectedLanguageChangedEvent
slug: telerikjustdecompilehelp/events/selectedlanguagechangedevent
tags: selectedlanguagechangedevent
published: True
position: 0
---

# SelectedLanguageChangedEvent



This class provides a push notification to all of the clients subscribers, when file(s) are loaded/removed from/to JustDecompile.
      Event base notification is dispatched to all of the subscribers.
    

## Syntax:

	
          public class TreeViewItemCollectionChangedEvent : CompositePresentationEvent<IEnumerable<ITreeViewItem>>
          {
          }
          
          public interface ITreeViewItem
		  {
		        TreeNodeType TreeNodeType { get; }
		  }
        



	
          Public Class TreeViewItemCollectionChangedEvent
                Inherits CompositePresentationEvent(Of IEnumerable(Of ITreeViewItem))
          End Class
          
          Public Interface ITreeViewItem
				ReadOnly Property TreeNodeType() As TreeNodeType
		  End Interface
        



## Example:

	
          public void OnImportsSatisfied()
          {
              this.eventAggregator.GetEvent<TreeViewItemCollectionChangedEvent>().Subscribe(OnTreeViewItemCollectionChangedEvent);
          }

          private void LoadAssembliesIntoPlugin(IEnumerable<ITreeViewItem>assemblies)
          {
              this.assemblies = assemblies;
          }
        



	
          Public Sub OnImportsSatisfied()
              Me.eventAggregator.GetEvent(Of TreeViewItemCollectionChangedEvent)().Subscribe(New Action(Of IEnumerable(Of ITreeViewItem))(AddressOf OnTreeViewItemCollectionChanged))
          End Sub

          Private Sub LoadAssembliesIntoPlugin(assemblies As IEnumerable(Of ITreeViewItem))
              Me.assemblies = assemblies
          End Sub
        


