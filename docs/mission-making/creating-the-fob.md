# Creating the FOB

Every mission needs a FOB. This is where players will spawn, and where they will return to after completing objectives. The FOB is also where players will be able to access the shop, and where vehicles will be spawned.

## Pick a location

A FOB should be within a reasonable distance from the AO, but far enough away that the enemies will not be alerted to the FOB's presence.

A good FOB location:
- Is a reasonably flat area
- Is at least 2km from the AO
- Is not too close to any civilian areas
- Has access to a road

## Place the Contractors

Place the contractors in the FOB. These are the units that players will be able to control. They should be placed without colliding with any other objects.

<video width="99%" loop muted markdown="1" controls>
    <source src="../videos/arma3_fob_players.webm" type="video/webm" markdown="1">
</video>

1. Place the player group, found in `Compositions > Independent > Synixe Contractors > Base Components > Players`
2. Highlight all units in the group.
3. Right click on one of the units, select `Attributes`
4. Change `Callsign` to `Synixe`
5. Navigate down to the `Object: Control` section
6. Check `Playable`
7. Set the Role Description to `Contractor`

## Respawns

By default, no respawn setup is needed. Players will respawn where their player started.

You can alternatively set up respawn points.

### Default Respawn

<video width="99%" loop muted markdown="1" controls>
    <source src="../videos/arma3_fob_respawn_default.webm" type="video/webm" markdown="1">
</video>

1. Place a `Respawn` object, found in `Objects > Props > Synixe Contractors > Helpers`.

That is it! Players will now respawn at the location of the `Respawn` object.

If you place multiple `Respawn` objects, players will respawn at a random one.

### Triggered Respawn

It is possible to change the respawn points based on a trigger.

<video width="99%" loop muted markdown="1" controls>
    <source src="../videos/arma3_fob_respawn_triggered.webm" type="video/webm" markdown="1">
</video>

1. Place a `Respawn` object, found in `Objects > Props > Synixe Contractors > Helpers`.
2. Place a `Trigger`, configure it to your liking.
3. Sync the `Respawn` objects to the `Trigger`.

When the trigger is activated, any synced `Respawn` objects will become the only active respawn points.
