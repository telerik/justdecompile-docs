---
title: Assembly Tree Context Menu
page_title: Assembly Tree Context Menu | JustDecompile Documentation
description: Documentation page about Assembly Tree Context Menu.
previous_url: /ui-regions-assembly-tree-context-menu.html
slug: assembly-tree-context-menu
published: True
position: 1
---

# Assembly Tree Context Menu



JustDecompile employs a hierachy of context menus to enable a number of useful actions in the assembly list navigation tree. A number of [Prism](https://compositewpf.codeplex.com/) regions are defined in this hierarchy thus enabling plugins to insert their own menu items at any level.

The menu items residing in the regions listed below should implement the [IMenuItem](/api/t_justdecompile_api_core_imenuitem) interface.

*   **AssemblyTreeViewContextMenuRegion:** All of the UI elements placed in this region will pop up in the assembly treeview item's context menu.

    ![Assembly Tree View Context Menu Region](/media/AssemblyTreeViewContextMenuRegion.png)

*   **ModuleDefinitionTreeViewContextMenuRegion:** All of the UI elements placed in this region will pop up in the context menu displayed over assembly's module definition treeview item.

    ![Module Definition Tree View Context Menu Region](/media/ModuleDefinitionTreeViewContextMenuRegion.png)

*   **AssemblyReferenceTreeViewContextMenuRegion:** All of the UI elements placed in this region will pop up in the context menu displayed over an assembly reference treeview item.

    ![Assembly Reference Tree View Context Menu Region](/media/AssemblyReferenceTreeViewContextMenuRegion.png)

*   **UnResolvedAssemblyReferenceTreeViewContextMenuRegion:** All of the UI elements placed in this region will pop up in the context menu displayed over an unresolved (i.e. which location is unknown to JustDecompile) assembly reference treeview item.

    ![Un Resolved Assembly Reference Tree View Context Menu Region](/media/UnResolvedAssemblyReferenceTreeViewContextMenuRegion.png)

*   **NamespaceTreeViewContextMenuRegion:** All of the UI elements placed in this region will pop up in the context menu displayed over a namespace treeview item.

    ![Namespace Tree View Context Menu Region](/media/NamespaceTreeViewContextMenuRegion.png)

*   **TypeTreeViewContextMenuRegion:** All of the UI elements placed in this region will pop up in the context menu displayed over a type treeview item.

    ![Type Tree View Context Menu Region](/media/TypeTreeViewContextMenuRegion.png)

*   **BaseTypeTreeViewContextMenuRegion:** All of the UI elements placed in this region will pop up in the context menu displayed over a base type treeview item.

    ![Base Type Tree View Context Menu Region](/media/BaseTypeTreeViewContextMenuRegion.png)

*   **InheritTreeViewContextMenuRegion:** All of the UI elements placed in this region will pop up in the context menu displayed over a derived type treeview item.

    ![Inherit Tree View Context Menu Region](/media/InheritTreeViewContextMenuRegion.png)

*   **MemberTreeViewContextMenuRegion:** All of the UI elements placed in this region will pop up in the context menu displayed over any type member treeview item.

    ![Member Tree View Context Menu Region](/media/MemberTreeViewContextMenuRegion.png)

*   **DefaultResourceTreeViewContextMenuRegion:** All of the UI elements placed in this region will pop up in the context menu displayed over a resource collection treeview item.

    ![Default Resource Tree View Context Menu Region](/media/DefaultResourceTreeViewContextMenuRegion.png)

*   **ResourceTreeViewContextMenuRegion:** All of the UI elements placed in this region will pop up in the context menu displayed over a assembly resource treeview item.

    ![Resource Tree View Context Menu Region](/media/ResourceTreeViewContextMenuRegion.png)

*   **EmbeddedResourceTreeViewContextMenuRegion:** All of the UI elements placed in this region will pop up in the context menu displayed over a child assembly resource treeview item.

    ![Embedded Resource Tree View Context Menu Region](/media/EmbeddedResourceTreeViewContextMenuRegion.png)

*   **XapTreeViewContextMenuRegion:** All of the UI elements placed in this region will pop up in the context menu displayed over a Silverlight XAP treeview item.

    ![Xap Tree View Context Menu Region](/media/XapTreeViewContextMenuRegion.png)

Tip |
--- |
| The plugin view model should implement [INotifyPropertyChanged](https://msdn.microsoft.com/en-us/library/system.componentmodel.inotifypropertychanged.aspx) interface, when it needs to provide dynamic property notification to the UI region where it's injected in.
