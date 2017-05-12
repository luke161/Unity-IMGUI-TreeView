# Unity-IMGUI-TreeView
Simple Tree View implementation for IMGUI (Editor GUI) in Unity. Includes a special type for working with asset paths, but base data structure and view can be easily extended to support anything.

Built and tested in **Unity 5.6.0**

![Screenshot](/Images/Screenshot.png)

## Usage
The Tree View is made up of two parts, a tree data structure [TreeNode](./Assets/TreeView/Scripts/TreeNode.cs) and an IMGUI control [TreeIMGUI](./Assets/TreeView/Editor/TreeIMGUI.cs). The project comes with a basic tree data structure which can be easily extended or wrapped in a container class (demonstrated with [AssetTree](./Assets/TreeView/Editor/AssetTree.cs)).

The IMGUI control produces a basic tree layout with foldout support, it can be easily extended to customise the appearance of rows by overriding `OnDrawTreeNode` and for more advanced layouts `OnDrawRow` and `OnGetLayoutHeight`.
For the standard IMGUI control to work data contained within a [TreeNode](./Assets/TreeView/Scripts/TreeNode.cs) must implement the [ITreeIMGUIData](./Assets/TreeView/Editor/TreeIMGUI.cs) interface. 

## Example
The project contains an example implementation [AssetTreeWindow](./Assets/TreeView/Example/Editor/AssetTreeEditorWindow.cs) which demonstrates how a tree view can be used to list asset search results. The example can be loaded via the Unity editor window under `Tools/Tree View Example Window`.
