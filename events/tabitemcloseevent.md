---
title: TabItemCloseEvent
page_title: TabItemCloseEvent | JustDecompile Documentation
description: Documentation page about TabItemCloseEvent.
previous_url: /events-tabitemcloseevent.html
slug: tabitemcloseevent
published: True
position: 4
---

# TabItemCloseEvent



This class provides a push notification to all of the clients subscribers, when particular tab item has been closed in JustDecompile.

Event base notification is dispatched to all of the subscribers.

## Syntax

<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve"><span class="highlight-keyword">public</span> <span class="highlight-keyword">class</span> TabItemCloseEvent : CompositePresentationEvent&lt;ITabItem&gt;
{
}</pre></td></tr></table></span></div>

## Example


 *You can subscribe to this event using the following code:* 


<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve"><span class="highlight-keyword">public</span> <span class="highlight-keyword">void</span> OnImportsSatisfied()
{
   <span class="highlight-keyword">this</span>.eventAggregator.GetEvent&lt;TabItemCloseEvent&gt;().Subscribe(OnTabItemClosed);
}</pre></td></tr></table></span></div>


An [ITabItem](/api/t_justdecompile_api_core_itabitem) instance is provided by JustDecompile to all of the event subscribers. It contains the tab item that will be closed in the application.

