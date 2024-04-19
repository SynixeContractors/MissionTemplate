# Action

A simple function for creating an ACE interaction menu action on an object.

## Parameters

- `object`: Object - The object to attach the action to.
- `title`: String - The action name.
- `action`: Code - The action to perform when the action is selected.
- `repeatable`: Boolean - Whether the action can be repeated. Default is `false`.
- `condition`: Code - The condition that must be met for the action to be available. Default is `{true}`.
- `icon`: String - The icon to display next to the action. Default is the dot.

## Action Code

The code will only run on the client that activated the action, make sure to
take this into account and ask for help if you are unsure how to
handle this in your code.

Inside the code, you have access to two variables:

- `_player`: Object - The player who activated the action.
- `_target`: Object - The object the action was activated on.

## Example

[Example Mission](https://github.com/SynixeContractors/Missions/tree/main/examples/FunctionAction.Stratis)

In this short example, a laptop is used to trigger explosives on a fuel truck.

The player can interact with the laptop, and will play a gesture while the fuel
truck is destroyed.

Because the `repeatable` parameter is not set, the action will disappear when it
is used.

**initPlayerLocal.sqf**
```sqf
[
    this,
    "Press Enter",
    {
        [_player, "PutDown"] call ace_common_fnc_doGesture;
        fueltruck setDamage 1;
    }
] call synixe_missions_fnc_action;
```

<video width="99%" loop muted markdown="1" controls>
    <source src="../../videos/fnc_synixe_action.webm" type="video/webm" markdown="1">
</video>
