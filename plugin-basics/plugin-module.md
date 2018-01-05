---
title: Plugin Module
page_title: Plugin Module | UI for ASP.NET AJAX Documentation
description: Plugin Module
slug: telerikjustdecompilehelp/plugin-basics/plugin-module
tags: plugin,module
published: True
position: 0
---

# Plugin Module






        JustDecompile leverages           
        [MEF](http://mef.codeplex.com/)
        and
        [Prism](http://compositewpf.codeplex.com/)  for discovering, loading and composing any plugins and their corresponding dependencies.
        


          A plugin is a Prism module exposed through MEF. 
        


          To be exposed as Prism module the plugin should contain a class marked with the ModuleExport attribute and implementing the IModule interface (see the example below). The Initialize() method of that class 
          will be called as soon as JustDecompile loads the plugin in its application domain. At this point the plugin can commence executing its custom logic.
        

	
	    		[ModuleExport(typeof(PluginModule))]
			    public class PluginModule : IModule
			    {
			    	public void Initialize()
			    	{
			    		// Put your initialization logic here.
			    	}
			    }
				



	
					<ModuleExport(GetType(PluginModule))> _
					Public Class PluginModule
						Implements IModule
			    
						Public Sub Initialize()
							'Put your initialization logic here.
						End Sub
						
					End Class
				


