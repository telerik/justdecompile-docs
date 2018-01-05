---
title: SelectedTreeViewItemChangedEvent
page_title: SelectedTreeViewItemChangedEvent | UI for ASP.NET AJAX Documentation
description: SelectedTreeViewItemChangedEvent
slug: telerikjustdecompilehelp/events/selectedtreeviewitemchangedevent
tags: selectedtreeviewitemchangedevent
published: True
position: 4
---

# SelectedTreeViewItemChangedEvent



This class provides a push notification to all of the clients subscribers, when a new tab item is created in JustDecompile.
   

## Syntax:

	
         public class TabItemOpenEvent : CompositePresentationEvent<ITabItem>
         {
         }
       



	
         Public Class TabItemOpenEvent
              Inherits CompositePresentationEvent(Of ITabItem)
         End Class
       



## Example:

*You can subscribe to this event using the following code:*

	
         public void OnImportsSatisfied()
         {
            this.eventAggregator.GetEvent<TabItemOpenEvent>().Subscribe(OnTabItemOpen);
         }
       



	
         Public Sub OnImportsSatisfied()
            Me.eventAggregator.GetEvent(Of TabItemOpenEvent)().Subscribe(New Action(Of ITreeViewItem)(AddressOf OnTabItemOpen))
         End Sub
       



An T:JustDecompile.API.Core.ITabItem
         instance is provided by JustDecompile to all of the event subscribers.
         It contains the tab item that will be opened in the application.
       
