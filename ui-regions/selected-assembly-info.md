---
title: Selected Assembly Info
page_title: Selected Assembly Info | UI for ASP.NET AJAX Documentation
description: Selected Assembly Info
slug: telerikjustdecompilehelp/ui-regions/selected-assembly-info
tags: selected,assembly,info
published: True
position: 3
---

# Selected Assembly Info



__The UI elements placed in this region will pop up in the selected assembly info area.__![assemblyinfo](images/images/assemblyinfo.png)__Example__

__Code implementaion:__

	
          [ModuleExport(typeof(PluginModule))]
          public class PluginModule : IModule, IPartImportsSatisfiedNotification
          {
              public void OnImportsSatisfied()
              {
                  this.regionManager.AddToRegion("AssemblyInfoRegion", AssemblyInfoRegionView);
              }
          }
        



	
          <ModuleExport(GetType(PluginModule))> _
          Public Class PluginModule
              Implements IModule
              Implements IPartImportsSatisfiedNotification

              Public Sub OnImportsSatisfied()
                  Me.regionManager.AddToRegion("AssemblyInfoRegion", AssemblyInfoRegionView)
              End Sub

          End Class
        


