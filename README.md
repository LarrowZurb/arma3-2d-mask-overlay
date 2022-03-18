# Arma 3 - [MP Compatbile] Gas Mask/Helmet Overlay
This is a heavily modified version of the overlay from the script "Radiation - DEMO" made by ALIAS.
The script is intended for use with multiplayer missions. With minor modification the script will work with singleplayer.

## How to use
Edit gasmask.sqf and change line 4 to the equipment you want to trigger the overlay.
In the below example the equipment is set to G_Balaclava_blk
`protection = "G_Balaclava_blk";` 

Change line 28  from `(goggles _unit isEqualTo protection)` to `(headgear _unit isEqualTo protection)` if the item which you want is located in a different slot, like headgear.

## Notes:
If you wish to use the Arma 3 Contact DLC cbrn gear, keep in mind that the unit (cbrn_specialist) spawns with "G_AirPurifyingRespirator_01_nofilter_F" and later respawns with "G_AirPurifyingRespirator_01_F".


## Features:
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

## Credits for the original script to ALIAS.
https://steamcommunity.com/sharedfiles/filedetails/?id=909790601
