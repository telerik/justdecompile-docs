---
title: SelectedLanguageChangedEvent
page_title: SelectedLanguageChangedEvent | JustDecompile Documentation
description: Documentation page about SelectedLanguageChangedEvent.
previous_url: /events-selectedlanguagechangedevent.html
slug: selectedlanguagechangedevent
published: True
position: 1
---

# SelectedLanguageChangedEvent



This class provides a push notification to all of the clients subscribers, when programming language has been changed in JustDecompile.

Event base notification is dispatched to all of the subscribers.

## Syntax

<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td>

<pre>
    public class SelectedLanguageChangedEvent : CompositePresentationEvent<ILanguage>
    {
    }

    public interface ILanguage
    {
        Languages SelectedLanguage { get; }
    }

    public enum Languages
    {
        VisualBasic,
        CSharp,
        MSIL
    }
</pre>
</td></tr></table></span></div>

## Example

 *You can subscribe to this event using the following code:* 

<div id="syntaxCodeBlocks" class="code"><span codeLanguage="CSharp"><table><tr><th>C#</th></tr><tr><td>

<pre>
    public void OnImportsSatisfied()
    {
        this.eventAggregator.GetEvent<SelectedLanguageChangedEvent>().Subscribe(OnLanguageChanged);
    }

    private void OnLanguageChanged(ILanguage language)
    {
        switch (language.SelectedLanguage)
        {
            case Languages.VisualBasic:
            break;

            case Languages.CSharp:
            break;

            case Languages.MSIL:
            break;

            default:
            break;
        }

</pre>
</td></tr></table></span></div>


An [ILanguage](/api/t_justdecompile_api_core_ilanguage) instance is provided by JustDecompile to all of the event subscribers. It contains the currently selected programming language in the application.


