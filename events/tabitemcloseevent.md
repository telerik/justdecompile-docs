---
title: TabItemCloseEvent
page_title: TabItemCloseEvent | UI for ASP.NET AJAX Documentation
description: TabItemCloseEvent
slug: telerikjustdecompilehelp/events/tabitemcloseevent
tags: tabitemcloseevent
published: True
position: 3
---

# TabItemCloseEvent



This class provides a push notification to all of the clients subscribers, when particular tab item has been closed in JustDecompile.
   

## Syntax:

	
         public class TabItemCloseEvent : CompositePresentationEvent<ITabItem>
         {
         }
       



	
         Public Class TabItemCloseEvent
              Inherits CompositePresentationEvent(Of ITabItem)
         End Class
       



## Example:

*You can subscribe to this event using the following code:*

	
         public void OnImportsSatisfied()
         {
            this.eventAggregator.GetEvent<TabItemCloseEvent>().Subscribe(OnTabItemClosed);
         }
       



	
         Public Sub OnImportsSatisfied()
            Me.eventAggregator.GetEvent(Of TabItemCloseEvent)().Subscribe(New Action(Of ITreeViewItem)(AddressOf OnTabItemClosed))
         End Sub
       



An T:JustDecompile.API.Core.ITabItem
         instance is provided by JustDecompile to all of the event subscribers.
         It contains the tab item that will be closed in the application.
       
