# Arma 3 - [MP Compatbile] Gas Mask/Helmet Overlay
This is a heavily modified version of the overlay from the script "Radiation - DEMO" made by ALIAS.
The script is intended for use with multiplayer missions. With minor modification the script will work with singleplayer.

When a player respawns the player object is changed to new one, this esentially renderes scripts for overlay useless in mulitplayer.
To overcome this, the script uses a Respawn Handler created in the unit_init.sqf. When a player respawns the handler invokes the gasmask.sqf with arguments pointing to the current player object.

## How to use
Edit gasmask.sqf and change line 4 to the equipment you want to trigger the overlay.
In the below example the equipment is set to G_Balaclava_blk
`protection = "G_Balaclava_blk";` 

Change line 28  from `(goggles _unit isEqualTo protection)` to `(headgear _unit isEqualTo protection)` if the item which you want is located in a different slot, like headgear.

## Notes:
* If you wish to use the Arma 3 Contact DLC cbrn gear, keep in mind that the unit (cbrn_specialist) spawns with "G_AirPurifyingRespirator_01_nofilter_F" and later respawns with "G_AirPurifyingRespirator_01_F".
* If you whish to change the default sounds provided with this script, you can find free samples here https://freesound.org/home/. Audacity can be used to edit the sound according to your needs and exported to .ogg format.


## Features:
* gasmask.sqf compiled to memory and lodaded from there instead of reading from disk each time.
* Custom overlays
* Custom sounds for equip/uneqip & breathing.
* Multiplayer compatible
* Compatible with respawns



## Known issues:
* Gas mask overlay will remain after respawn until the player equips and then unequips the "Gas mask"

## To-Do:
* Remove the overlay effect after respawn
* Optimize the code to have less impact on the client
* Create a singleplayer version of this script

## Lessons learned:
* gasmask.sqf and unit_init.sqf had functions with the same name "fnc_overlay". This essentially froze the script, keep that in mind if you modify this script.

## Credits for the original script to ALIAS.
https://steamcommunity.com/sharedfiles/filedetails/?id=909790601
