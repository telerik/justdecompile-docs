---
title: Codeviewer Plugins Area
page_title: Codeviewer Plugins Area | UI for ASP.NET AJAX Documentation
description: Codeviewer Plugins Area
slug: telerikjustdecompilehelp/ui-regions/codeviewer-plugins-area
tags: codeviewer,plugins,area
published: True
position: 2
---

# Codeviewer Plugins Area



__The UI elements placed in this region will pop up under the main code viewer area.__![Code Viewer Plugin Area](images/images/CodeViewerPluginArea.png)

__Example__

	
              [ModuleExport(typeof(PluginModule))]
              public class PluginModule : IModule, IPartImportsSatisfiedNotification
              {
                  public void OnImportsSatisfied()
                  {
                      this.regionManager.AddToRegion("PluginRegion", PluginRegionView);
                  }
              }
         



	
              <ModuleExport(GetType(PluginModule))> _
              Public Class PluginModule
                  Implements IModule
                  Implements IPartImportsSatisfiedNotification

                  Public Sub OnImportsSatisfied()
                      Me.regionManager.AddToRegion("PluginRegion", PluginRegionView)
                  End Sub
              End Class
            


