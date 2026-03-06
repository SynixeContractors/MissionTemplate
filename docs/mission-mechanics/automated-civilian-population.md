# Automated civilian population

## Enabling GRAD CIVS

GRAD CIVS is a useful addon that brings a functionality to make the ambience of
a virtual world more lively by populating it with civilians.

If you would like to enable it on your mission, you can go to
`Settings > Addon Options > Mission` and then make sure you tick on the
checkbox to `Enable GRAD_CIVS`.

## GRAD CIVS Population types

GRAD CIVS will by default populate the whole world when enabled, however, we can
further fine-tune how we want it to handle our civilian population.

To do this, you'll want to place down a `Trigger` and choose it's size, which will
define how much of an area we will affect, then, we will place either a
`Population zone` or an `Exclusion zone` module from the ´GRAD CIVS´ category.

Placing a `Population zone` will make GRAD CIVS only spawn civilians in the areas
you define, and nowhere else, as opposed to populating the whole map as needed.

Placing an `Exclusion zone` will prevent GRAD CIVS from spawning civilians within
the areas you defined.

## GRAD CIVS Transit

If you want to define a main route of transit utilizing GRAD CIVS, you will
use the `Transit Traffic Source` and `Transit Traffic Sink` modules.

`Transit Traffic Source` will define where vehicles will spawn and start at, while
`Transit Traffic Sink` will define where vehicles' destination will be and where
they will despawn. You will have to `Connect > Sync to` each Source module to their
corresponding Sink module.

```admonish
You should prefferably put the Source and Sink in places where players will not
run into them, like outside the area of operations; otherwise, players will see
where vehicles spawn and despawn, thus ruining their immersion.
```

## GRAD CIVS Classes

To set the civilians that will spawn, place down the units you'd like it to pick from.

If you want 50% of your civilians to be wearing polos, 25% in summer clothing, and
25% in construction gear, you'd place down two polos, one summer, one construction
from your desired civilian identity. Select all the units, right click, and select
`Log > Log Classes as String to Clipboard`.

Then go into `Settings > Addon Options > Mission`, and then click the dropdown
menu and find GRAD CIVS.

If you want to define the pedestrians you'd like to be spawned, paste the code
in the `Unit classes to use for spawning civilians` field.

You can also define vehicles using the same method, and paste the code in the
`Vehicles that civilians may drive (class names)` field.

If you want to define a chance for your pedestrians to use backpacks, paste
the code below in the `Backpacks that civilians may wear` field.

~~~admonish collapsible=true title="BACKPACK presets"
BACKPACKS

```sqf
B_Messenger_Black_F, B_Messenger_Coyote_F, B_Messenger_Gray_F,
B_Messenger_Olive_F, B_CivilianBackpack_01_Everyday_Black_F,
B_CivilianBackpack_01_Sport_Blue_F, B_CivilianBackpack_01_Sport_Green_F,
B_CivilianBackpack_01_Sport_Red_F
```
~~~
