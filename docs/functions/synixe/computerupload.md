# Computer Upload

An interaction on a laptop for the players to "hack" and upload data.

## Parameters

- `object`: Object - The laptop object.
- `textureSource`: Number - The texture source for the laptop screen.
- `filesize`: Number - The size of the file to upload in gigabytes.
- `uploadTime`: Number - The time it takes to upload the file in seconds.
- `onStart`: Code - Code to run when the upload starts.
- `onComplete`: Code - Code to run when the upload completes.
- `host`: String - Host name to display on the laptop screen. Default: `localhost`.
- `user`: String - User name to display on the laptop screen. Default: `root`.

The texture source is the index of the texture in the `textures` array of the
model. You can find this by looking at the object in the editor.

![Texture Source](computerupload-textureindex.png)

In this example, the texture source is 1.

## On Start & On Complete Code

The code will only run on the server, make sure to take this into account and
ask for help if you are unsure how to handle this in your code.

Inside the code, you'll have `_this` available, which has the following properties:

- `_object`: Object - The laptop object.

## Example

[Example Mission](https://github.com/SynixeContractors/Missions/tree/main/examples/FunctionComputerUpload.Stratis)

In this example, the player interacts with a laptop to upload a file. After the
upload, the laptop screen will go black.

**init.sqf**
```sqf
[
    laptop,
    1,  // texture source
    50, // size in GB
    8,  // time to upload in seconds
    {
        systemChat "Server: Upload Started";
    },
    {
        systemChat "Server: Upload Finished";
        // Clear the screen after 2 seconds
        [{
            params ["_object"];
            _object setObjectTextureGlobal [1, ""];
        }, _this, 2] call CBA_fnc_waitAndExecute;
    }
] call synixe_missions_fnc_computerUpload;
```

<video width="99%" loop muted markdown="1" controls>
    <source src="../../videos/fnc_synixe_computerUpload.webm" type="video/webm" markdown="1">
</video>
