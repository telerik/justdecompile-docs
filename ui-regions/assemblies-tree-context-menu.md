---
title: Assemblies Tree Context Menu
page_title: Assemblies Tree Context Menu | UI for ASP.NET AJAX Documentation
description: Assemblies Tree Context Menu
slug: telerikjustdecompilehelp/ui-regions/assemblies-tree-context-menu
tags: assemblies,tree,context,menu
published: True
position: 0
---

# Assemblies Tree Context Menu



JustDecompile employs a hierachy of context menus to enable a number of useful actions in the assembly list navigation tree. A number of
        [Prism](http://compositewpf.codeplex.com/) regions are defined in this hierarchy thus enabling plugins to insert their own menu items at any level.
    

The menu items residing in the regions listed below should implement the T:JustDecompile.API.Core.IMenuItem   interface.
    

* __AssemblyTreeViewContextMenuRegion:__
          All of the UI elements placed in this region will pop up in the assembly treeview item's context menu.
        ![Assembly Tree View Context Menu Region](images/images/TreeViewContextMenu/AssemblyTreeViewContextMenuRegion.png)

* __ModuleDefinitionTreeViewContextMenuRegion:__
          All of the UI elements placed in this region will pop up in the context menu displayed over assembly's module definition treeview item.
        ![Module Definition Tree View Context Menu Region](images/images/TreeViewContextMenu/ModuleDefinitionTreeViewContextMenuRegion.png)

* __AssemblyReferenceTreeViewContextMenuRegion:__
          All of the UI elements placed in this region will pop up in the context menu displayed over an assembly reference treeview item.
        ![Assembly Reference Tree View Context Menu Region](images/images/TreeViewContextMenu/AssemblyReferenceTreeViewContextMenuRegion.png)

* __UnResolvedAssemblyReferenceTreeViewContextMenuRegion:__
          All of the UI elements placed in this region will pop up in the context menu displayed over an unresolved (i.e. which location is unknown to JustDecompile) assembly reference treeview item.
        ![Un Resolved Assembly Reference Tree View Context Menu Region](images/images/TreeViewContextMenu/UnResolvedAssemblyReferenceTreeViewContextMenuRegion.png)

* __NamespaceTreeViewContextMenuRegion:__
          All of the UI elements placed in this region will pop up in the context menu displayed over a namespace treeview item.
        ![Namespace Tree View Context Menu Region](images/images/TreeViewContextMenu/NamespaceTreeViewContextMenuRegion.png)

* __TypeTreeViewContextMenuRegion:__
          All of the UI elements placed in this region will pop up in the context menu displayed over a type treeview item.
        ![Type Tree View Context Menu Region](images/images/TreeViewContextMenu/TypeTreeViewContextMenuRegion.png)

* __BaseTypeTreeViewContextMenuRegion:__
          All of the UI elements placed in this region will pop up in the context menu displayed over a base type treeview item.
        ![Base Type Tree View Context Menu Region](images/images/TreeViewContextMenu/BaseTypeTreeViewContextMenuRegion.png)

* __InheritTreeViewContextMenuRegion:__
          All of the UI elements placed in this region will pop up in the context menu displayed over a derived type treeview item.
        ![Inherit Tree View Context Menu Region](images/images/TreeViewContextMenu/InheritTreeViewContextMenuRegion.png)

* __MemberTreeViewContextMenuRegion:__
          All of the UI elements placed in this region will pop up in the context menu displayed over any type member treeview item.
        ![Member Tree View Context Menu Region](images/images/TreeViewContextMenu/MemberTreeViewContextMenuRegion.png)

* __DefaultResourceTreeViewContextMenuRegion:__
          All of the UI elements placed in this region will pop up in the context menu displayed over a resource collection treeview item.
        ![Default Resource Tree View Context Menu Region](images/images/TreeViewContextMenu/DefaultResourceTreeViewContextMenuRegion.png)

* __ResourceTreeViewContextMenuRegion:__
          All of the UI elements placed in this region will pop up in the context menu displayed over a assembly resource treeview item.
        ![Resource Tree View Context Menu Region](images/images/TreeViewContextMenu/ResourceTreeViewContextMenuRegion.png)

* __EmbeddedResourceTreeViewContextMenuRegion:__
          All of the UI elements placed in this region will pop up in the context menu displayed over a child assembly resource treeview item.
        ![Embedded Resource Tree View Context Menu Region](images/images/TreeViewContextMenu/EmbeddedResourceTreeViewContextMenuRegion.png)

* __XapTreeViewContextMenuRegion:__
          All of the UI elements placed in this region will pop up in the context menu displayed over a Silverlight XAP treeview item.
        ![Xap Tree View Context Menu Region](images/images/TreeViewContextMenu/XapTreeViewContextMenuRegion.png)

>tip  *The plugin view model should implement[INotifyPropertyChanged](http://msdn.microsoft.com/en-us/library/system.componentmodel.inotifypropertychanged.aspx)interface,
			      when it needs to provide dynamic property notification to the UI region where it's injected in.* 
>

