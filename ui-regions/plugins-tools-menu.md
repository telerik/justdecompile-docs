---
title: Plugins Tools Menu
page_title: Plugins Tools Menu | UI for ASP.NET AJAX Documentation
description: Plugins Tools Menu
slug: telerikjustdecompilehelp/ui-regions/plugins-tools-menu
tags: plugins,tools,menu
published: True
position: 1
---

# Plugins Tools Menu



__The UI elements placed in this region will pop up in the top level toolbar menu area.__

The menu items residing in this region should implement the T:JustDecompile.API.Core.IMenuItem   interface.
    ![Toolbar](images/images/Toolbar.png)__Example__

__Code implementaion:__

	
          [ModuleExport(typeof(PluginModule))]
          public class PluginModule : IModule, IPartImportsSatisfiedNotification
          {
              public void OnImportsSatisfied()
              {
                  this.regionManager.AddToRegion("ToolMenuRegion", ToolMenuItem);
              }
          }
        



	
          <ModuleExport(GetType(PluginModule))> _
          Public Class PluginModule
            Implements IModule
            Implements IPartImportsSatisfiedNotification

              Public Sub OnImportsSatisfied()
                  Me.regionManager.AddToRegion("ToolMenuRegion", ToolMenuItem)
              End Sub

          End Class
        



>tip  *The plugin view model should implement[INotifyPropertyChanged](http://msdn.microsoft.com/en-us/library/system.componentmodel.inotifypropertychanged.aspx)interface,
              when it needs to provide dynamic property notification to the UI region where it's injected in.* 
>

