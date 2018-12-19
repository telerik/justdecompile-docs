---
title: SelectedTabItemChangedEvent
page_title: SelectedTabItemChangedEvent | JustDecompile Documentation
description: Documentation page about SelectedTabItemChangedEvent.
previous_url: /events-selectedtabitemchangedevent.html
slug: selectedtabitemchangedevent
published: True
position: 3
---

# SelectedTabItemChangedEvent



This class provides a push notification to all of the clients subscribers, when selected tab item has been changed in JustDecompile.

Event base notification is dispatched to all of the subscribers.

## Syntax


<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve"><span class="highlight-keyword">public</span> <span class="highlight-keyword">class</span> SelectedTabItemChangedEvent : CompositePresentationEvent&lt;ITabItem&gt;
{
}</pre></td></tr></table></span></div>

## Example


 *You can subscribe to this event using the following code:* 

<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve"><span class="highlight-keyword">public</span> <span class="highlight-keyword">void</span> OnImportsSatisfied()
{
   <span class="highlight-keyword">this</span>.eventAggregator.GetEvent&lt;SelectedTabItemChangedEvent&gt;().Subscribe(OnTabItemChanged);
}</pre></td></tr></table></span></div>


An [ITabItem](/api/t_justdecompile_api_core_itabitem) instance is provided by JustDecompile to all of the event subscribers. It contains the currently selected tab item in the application.
