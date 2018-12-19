---
title: Overview
page_title: Events | JustDecompile Documentation
description: Documentation page about Events.
previous_url: /events.html
slug: overview
published: True
position: 0
---

# Events



## JustDecompile Events

JustDecompile uses the [Prism](https://compositewpf.codeplex.com/) event mechanism to notify a plugin about user actions and changes in the UI.This mechanism is based on the Event Aggregator service and allows publishers and subscribers to communicate through events and still do not have a direct reference to each other.

## Event Aggregator Service

An instance of the IEventAggregator is created by the MEF engine when application is started. Plugin module can get a reference to this instance by applying a local variable with an Import attribute.

<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve">[Import]
<span class="highlight-keyword">private</span> IEventAggregator eventAggregator;</pre></td></tr></table></span></div>

| Note |
| ---|
| MEF provides an IPartImportsSatisfiedNotification interface that enables implementers to be notified when a part's imports have been satisfied. It contains a single OnImportsSatisfied() method, which is called when a part's imports have been satisfied and it is safe to use. |

<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td><pre xml:space="preserve">[ModuleExport(<span class="highlight-keyword">typeof</span>(PluginModule))]
<span class="highlight-keyword">public</span> <span class="highlight-keyword">class</span> PluginModule : IModule, IPartImportsSatisfiedNotification
{
    <span class="highlight-keyword">public</span> <span class="highlight-keyword">void</span> OnImportsSatisfied()
    {
        <span class="highlight-keyword">this</span>.eventAggregator.GetEvent&lt;SelectedTreeViewItemChangedEvent&gt;().Subscribe(OnSelectedTreeViewItemChanged);
    }
    ......
}</pre></td></tr></table></span></div>


## Events List

JustDecompile defines the following Prism events that can be used as a communication channel between plugin module and JustDecompile application.

*   [SelectedLanguageChangedEvent](selectedlanguagechangedevent)

*   [SelectedTreeViewItemChangedEvent](selectedtreeviewitemchangedevent)

*   [TreeViewItemCollectionChangedEvent](treeviewitemcollectionchangedevent)

*   [SelectedTabItemChangedEvent](selectedtabitemchangedevent)

*   [TabItemCloseEvent](tabitemcloseevent)

*   [TabItemOpenEvent](tabitemopenevent)

