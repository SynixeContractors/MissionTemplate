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

## GRAD CIVS Presets

To use these presets, go into `Settings > Addon Options > Mission`, and then
click the dropdown menu and find GRAD CIVS.

If you want to define the pedestrians you'd like to be spawned, paste the code
in the `Unit classes to use for spawning civilians` field.

If you want to define the vehicles you'd like the pedestrians to use, paste the
code in the `Vehicles that civilians may drive (class names)` field.

Here are some presets we've made in the past for some of our missions, feel
free to use them in yours!

~~~admonish collapsible=true title="ALTIS preset"
ALTIS (Pedestrians)

```sqf
C_man_polo_1_F, C_man_polo_2_F, C_man_polo_3_F, C_man_polo_4_F, C_man_polo_5_F,
C_man_polo_6_F, C_man_polo_1_F_afro, C_man_polo_5_F_afro
```

ALTIS (Vehicles)

```sqf
C_Hatchback_01_F, C_SUV_01_F, C_Van_01_transport_F, C_Van_01_box_F, C_Offroad_01_F,
C_Offroad_02_unarmed_F, C_Pickup_covered_rf, C_Pickup_rf
```
~~~

~~~admonish collapsible=true title="TANOA preset (French Polynesia)"
Tanoa (Pedestrians)

```sqf
C_Man_casual_1_F_tanoan, C_Man_casual_2_F_tanoan, C_Man_casual_3_F_tanoan, 
C_Man_casual_4_v2_F_tanoan, C_Man_casual_5_v2_F_tanoan, C_Man_casual_6_v2_F_tanoan,
C_Man_casual_7_F_tanoan, C_Man_casual_9_F_tanoan, C_Man_casual_8_F_tanoan, 
C_man_sport_1_F_tanoan, C_man_sport_2_F_tanoan, C_man_sport_3_F_tanoan, 
C_Man_casual_4_F_tanoan, C_Man_casual_5_F_tanoan, C_Man_casual_6_F_tanoan, C_MU_man_random_civil_tanoan
```

Tanoa (Vehicles)

```sqf
C_Hatchback_01_F, C_SUV_01_F, C_Van_01_transport_F, C_Van_01_box_F,
C_Offroad_01_F, C_Offroad_02_unarmed_F, C_Pickup_covered_rf, C_Pickup_rf
```
~~~

~~~admonish collapsible=true title="AFRICAN preset"
AFRICAN (Pedestrians)

```sqf
C_man_polo_1_F_afro, C_man_polo_2_F_afro, C_man_polo_3_F_afro, C_man_polo_4_F_afro,
C_man_polo_5_F_afro, C_man_polo_6_F_afro, C_Man_casual_6_F_afro, C_Man_casual_5_F_afro,
C_Man_casual_4_F_afro
```

AFRICAN (Vehicles)

```sqf
C_Quadbike_01_F, C_Offroad_02_unarmed_F, C_Van_01_transport_F, C_Van_01_box_F, C_Tractor_01_F
```
~~~

~~~admonish collapsible=true title="ASIAN preset"
ASIAN (Pedestrians)

```sqf
C_Man_casual_1_F_asia, C_Man_casual_2_F_asia, C_Man_casual_3_F_asia
C_Man_casual_4_v2_F_asia, C_Man_casual_5_v2_F_asia, C_Man_casual_6_v2_F_asia
C_Man_casual_7_F_asia, C_Man_casual_8_F_asia, C_Man_casual_9_F_asia
```
~~~

~~~admonish collapsible=true title="CHERNARUS (CUP) preset"
CHERNARUS (Pedestrians, CUP)

```sqf
CUP_C_C_Bully_03, CUP_C_C_Bully_02, CUP_C_C_Citizen_01, CUP_C_C_Citizen_03,
CUP_C_C_Profiteer_02, CUP_C_C_Racketeer_01, CUP_C_C_Rocker_03, CUP_C_C_Villager_03,
CUP_C_C_Villager_04, CUP_C_C_Woodlander_03
```
~~~

~~~admonish collapsible=true title="LIVONIA preset"
LIVONIA (Pedestrians)

```sqf
C_Man_casual_2_F_euro, C_Man_casual_3_F_euro, C_Man_casual_6_v2_F_euro, C_Man_casual_7_F_euro,
C_Man_casual_8_F_euro, C_Man_formal_1_F_euro, C_Man_formal_4_F_euro, C_scientist_01_informal_F,
C_Man_2_enoch_F, C_Man_3_enoch_F, C_Man_1_enoch_F, C_Farmer_01_enoch_F
```

LIVONIA (Vehicles)

```sqf
C_Truck_02_covered_F, C_Truck_02_fuel_F, C_Offroad_01_F, C_Offroad_01_covered_F,
C_SUV_01_F, C_Van_01_transport_F, C_Van_01_box_F, C_Van_02_vehicle_F, C_Van_02_service_F,
C_Van_02_transport_F, C_Pickup_covered_rf, C_Pickup_rf
```
~~~

~~~admonish collapsible=true title="TAKISTAN (CUP) preset"
TAKISTAN (Pedestrians, CUP)

```sqf
CUP_C_TK_Man_06_Coat, CUP_C_TK_Man_06_Jack, CUP_C_TK_Man_06_Waist, CUP_C_TK_Man_05_Coat,
CUP_C_TK_Man_05_Jack, CUP_C_TK_Man_05_Waist, CUP_C_TK_Man_08, CUP_C_TK_Man_08_Jack,
CUP_C_TK_Man_08_Waist, CUP_C_TK_Man_07, CUP_C_TK_Man_07_Coat, CUP_C_TK_Man_07_Waist,
CUP_C_TK_Man_04, CUP_C_TK_Man_04_Jack, CUP_C_TK_Man_04_Waist, CUP_C_TK_Man_02,
CUP_C_TK_Man_02_Jack, CUP_C_TK_Man_02_Waist, CUP_C_TK_Man_01_Waist, CUP_C_TK_Man_01_Coat,
CUP_C_TK_Man_01_Jack, CUP_C_TK_Man_03_Coat, CUP_C_TK_Man_03_Jack, CUP_C_TK_Man_03_Waist
```
~~~

~~~admonish collapsible=true title="SEFROU-RAMAL (WS) preset"
SEFROU-RAMAL (Pedestrians, WS)

```sqf
C_Djella_01_lxWS, C_Djella_02_lxWS, C_Djella_03_lxWS, C_Djella_04_lxWS, 
C_Djella_05_lxWS,C_Tak_02_A_lxWS, C_Tak_02_B_lxWS, C_Tak_02_C_lxWS, 
C_Tak_03_A_lxWS, C_Tak_03_B_lxWS, C_Tak_03_C_lxWS, C_Tak_01_A_lxWS, 
C_Tak_01_B_lxWS, C_Tak_01_C_lxWs
```

SEFROU-RAMAL (Vehicles, WS)

```sqf
C_Van_01_transport_F, C_Van_01_box_F, C_Truck_02_flatbed_lxWS, 
C_Truck_02_cargo_lxWS, C_Offroad_01_F, C_Offroad_02_unarmed_F, C_Quadbike_01_F, C_Offroad_01_covered_F
```
~~~

If you want to define a chance for your pedestrians to use backpacks,
paste the code below in the `Backpacks that civilians may wear` field.

~~~admonish collapsible=true title="BACKPACK presets"
BACKPACKS

```sqf
B_Messenger_Black_F, B_Messenger_Coyote_F, B_Messenger_Gray_F,
B_Messenger_Olive_F, B_CivilianBackpack_01_Everyday_Black_F,
B_CivilianBackpack_01_Sport_Blue_F, B_CivilianBackpack_01_Sport_Green_F, B_CivilianBackpack_01_Sport_Red_F
```
~~~