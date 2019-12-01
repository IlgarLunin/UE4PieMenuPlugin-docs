# UE4 pie menu plugin documentation

![featured](img/featured.png)

This plugin adds blender-like radial menus to Unreal Engine 4 editor.

> Unlike blender, menus can be nested, like maya's markin menus.

> Menu entries are evenly distributed in a circle.

![nesting](img/nesting.gif)

For now there are 4 menus that can be invoked inside level editor viewport:
  * Modes menu
    ![nesting](img/modes.gif)
  * Python menu
    ![pyMenu2](img/pyMenu2.gif)
  * Shading menu
    ![shading](img/shading.gif)
  * Viewport type menu
    ![views](img/views.gif)

To summon particular menu, hit corresponding keyboard shortcut.

![shortcuts](img/shortcuts.png)

While buttons are pressed, move mouse pointer aside.

## How to setup python menu
Python menu is special one!

1) First of all, what you obviously want to do - is to enable PythonScriptPlugin.
![pyPlugin](img/pyPlugin.png)

2) Second - create python scripts to be added to menu. When command is activated, plugin will search `PieMenuEntry_` prefixed python scripts e.g. ("PieMenuEntry_MyUtil.py")
under following directories:
    * ProjectRoot/Content/Python
    * Plugin/Content/Python

For example, this file structure:

![pyMenuFIles](img/pyMenuFIles.png)

becomes a radial menu with single nested entry (*see first gif on this page*)
