# Speak

A function for creating an interaction on a unit to speak with them.

## Parameters

- `unit`: Object - The unit to attach the interaction to.
- `sound`: String - The sound to play when the interaction is selected.
- `onStart`: Code - Code to run when the unit starts speaking.
- `onDone`: Code - Code to run when the unit finishes speaking.
- `repeatable`: Boolean - Whether the interaction can be repeated. Default is `true`
- `condition`: Code - The condition for the interaction to be available. Default is `{true}`.
- `title`: String - The title of the interaction. Default is `Speak`.

## Start & Done Code

The code will only run on the server, make sure to take this into account and
ask for help if you are unsure how to handle this in your code.

Inside the code, you'll have `_this` available, which has the following properties:

- `_unit`: Object - The unit that is speaking.
- `_sound`: String - The sound that is playing.
- `_first`: Boolean - Whether this is the first time the sound is playing.
- `_duration`: Number - The duration of the sound in seconds.

## Example

[Example Mission](https://github.com/SynixeContractors/Missions/tree/main/examples/FunctionSpeak.Stratis)

In this example, the player interacts with an officer to hear them speak, and get
intel after the speech.

**description.ext**
```hpp
class CfgSounds {
    class Officer {
        name = "Officer";
        titles[] = {};
        sound[] = {
            "officer.ogg",  // Path to sound file
            5,              // Volume, 5 is recommended, always test in-game
            1               // Pitch
        };
        duration = 6;       // Duration of the sound in seconds
    };
};
```

**initPlayerLocal.sqf**
```sqf
[
    officer,    // variable name of the officer unit
    "Officer",  // class from CfgSounds in description.ext
    {
        systemChat "Officer: I'm talking";
    },
    {
        systemChat "Officer: I'm done";
        // The first time we interact, play an animation and give intel
        params ["_unit", "", "_first"];
        if (_first) then {
            [_unit, "PutDown"] call ace_common_fnc_doGesture;
            systemChat "Intel Received!";
        };
    }
] call synixe_missions_fnc_speak;
```

<video width="99%" loop muted markdown="1" controls>
    <source src="../../videos/fnc_synixe_speak.webm" type="video/webm" markdown="1">
</video>
