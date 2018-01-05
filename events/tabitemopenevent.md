---
title: TabItemOpenEvent
page_title: TabItemOpenEvent | UI for ASP.NET AJAX Documentation
description: TabItemOpenEvent
slug: telerikjustdecompilehelp/events/tabitemopenevent
tags: tabitemopenevent
published: True
position: 5
---

# TabItemOpenEvent



This class provides a push notification to all of the clients subscribers when the selected node in JustDecompile assembly list navigation tree changes.
    

## Syntax:

	
          public class SelectedTreeViewItemChangedEvent : CompositePresentationEvent<ITreeViewItem>
          {
          }
        



	
          Public Class SelectedTreeViewItemChangedEvent
          		Inherits CompositePresentationEvent(Of ITreeViewItem)
          End Class
        



## Example:

	
          public void OnImportsSatisfied()
          {
              this.eventAggregator.GetEvent<SelectedTreeViewItemChangedEvent>().Subscribe(OnTreeViewItemCollectionChangedEvent);
          }

          private void OnTreeViewItemCollectionChangedEvent(ITreeViewItem selectedTreeItem)
          {
              this.selectedTreeItem = selectedTreeItem;
          }
        



	
          Public Sub OnImportsSatisfied()
              Me.eventAggregator.GetEvent(Of SelectedTreeViewItemChangedEvent)().Subscribe(New Action(Of ITreeViewItem)(AddressOf OnTreeViewItemCollectionChangedHandler))
          End Sub

          Private Sub OnTreeViewItemCollectionChangedEvent(selectedTreeItem As ITreeViewItem)
              Me.selectedTreeItem = selectedTreeItem
          End Sub
        


