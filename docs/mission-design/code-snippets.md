# Code Snippets

## Easy plug-and-play coding snippets

Here are a few simple lines of code you can safely use to add unique gimmicks to your missions without adding too much complexity onto your workload! This is a compilation list of interesting things to put in an items's init field.

### Setting maximum speed on a vehicle

Do you want a vehicle to be slow, either due to heavy loads, malfunction, or other reasons? Try using putting this in it's init field:

```sqf
this setCruiseControl [40, false];
```

### Drag and load items with ACE

Do you want to add extra functionality for items you'd like players to be able to drag, carry, and load into vehicles? Try using any of the following in their init field!

If you want to make an item draggable, use:

```sqf
[this, true, [0, 1, 0]] call ace_dragging_fnc_setDraggable;
```

If you want to make an item carryable, use:

```sqf
[this, true, [0, 1, 0]] call ace_dragging_fnc_setCarryable;
```

If you want to make an item loadable into vehicles, use:

```sqf
[this, 1] call ace_cargo_fnc_setSize;
```

### Attaching objects to other objects

If you want to attach an object (1) to another object (2), you can use the following inside object (1)'s init field:

```sqf
[object1, object2] call BIS_fnc_attachToRelative;
```

```admonish info
Using this command keeps the relative positioning of the two objects: in other words, how you see them positioned in the 3DEN editor is how they will be attached when the game starts.
```
