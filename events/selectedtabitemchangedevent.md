---
title: SelectedTabItemChangedEvent
page_title: SelectedTabItemChangedEvent | UI for ASP.NET AJAX Documentation
description: SelectedTabItemChangedEvent
slug: telerikjustdecompilehelp/events/selectedtabitemchangedevent
tags: selectedtabitemchangedevent
published: True
position: 2
---

# SelectedTabItemChangedEvent



This class provides a push notification to all of the clients subscribers, when selected tab item has been changed in JustDecompile.
   

Event base notification is dispatched to all of the subscribers.
   

## Syntax:

	
         public class SelectedTabItemChangedEvent : CompositePresentationEvent<ITabItem>
         {
         }
       



	
         Public Class SelectedTabItemChangedEvent
              Inherits CompositePresentationEvent(Of ITabItem)
         End Class
       



## Example:

*You can subscribe to this event using the following code:*

	
         public void OnImportsSatisfied()
         {
            this.eventAggregator.GetEvent<SelectedTabItemChangedEvent>().Subscribe(OnTabItemChanged);
         }
       



	
         Public Sub OnImportsSatisfied()
            Me.eventAggregator.GetEvent(Of SelectedTabItemChangedEvent)().Subscribe(New Action(Of ITreeViewItem)(AddressOf OnTabItemChanged))
         End Sub
       



An T:JustDecompile.API.Core.ITabItem
         instance is provided by JustDecompile to all of the event subscribers.
         It contains the currently selected tab item in the application.
       
