# Includes for San Andreas Multiplayer+
San Andreas Multiplayer Includes Library+ or ISAMPP (Includes for San Andreas Multiplayer Plus) is 
library of include files for San Andreas Multiplayer Mod SA-MP. Purpose of ISAMPP is to make development 
of game modes for SA-MP much easier. SA-MP by default uses in most cases numeric identifiers which are 
hard to remember and without enough experience you have to use SA-MP wiki a lot. I believe that word 
identifiers are much more easier to remember, they make much more sense (especially if you are familiar with 
modding the game Grand Theft Auto: San Andreas) and may also have positive impact on your workflow.

Except re-definitions of numeric identifiers, ISAMPP also contains other useful libraries - such as library of 
locations with coordinates, interior identifiers and location names - or few related custom stock functions. 
ISAMPP is available with sandbox-styled game mode in which you can see everything implemented.

*ISAMPP is not part of San Andreas Multiplayer mod (SA-MP) and it is not affiliated with Rockstar
Games, Rockstar North or Take-Two Interactive Software Inc.*
*Grand Theft Auto and Grand Theft Auto: San Andreas are registered trademarks of Take-Two Interactive
Software Inc.*

*ISAMPP versions 1.3 or newer should be considered [public domain](LICENSE).*

<img src="docs/logo/isampp_logo_250px.png" width="100">

# Installation
Copy contents of include folder to *”[SA-MP Server folder]/include”* and also to *”include”* folder for Pawno *(by default ”[SA-MP Server folder]/pawno/include”)*.

In your game mode file you can include ISAMPP header for all its contents:

```#include <i_sampp>```

or include header files as you wish separately:

```#include <i_sampp/i_colorlist>
#include <i_sampp/i_iconids>
#include <i_sampp/i_locationids>
#include <i_sampp/i_pickupids>
#include <i_sampp/i_skinids>
#include <i_sampp/i_textstyle>
#include <i_sampp/i_vehids>
#include <i_sampp/i_vehhealth>
#include <i_sampp/i_carcols>
#include <i_sampp/i_paintjob>
#include <i_sampp/i_weaponids>
#include <i_sampp/i_weatherids>
```

If you wish to run included sandbox game mode, you have to add file ```testmpp.pwn``` to your *”gamemodes”* folder and compile it.
Alternatively, you can use pre-compiled file testmpp.amx.

# Includes

Every ISAMPP include file starts with prefix *'i_'*. Please keep in mind that ISAMPP may not be the only set of include files using this prefix.

*colorlist* - List of color definitions</br>
*iconids* - List of map icon identifiers</br>
*locationids* - List of location definitions with coordinates, interior identifiers and names</br>
*pickupids* - List of definitions for pickup identifiers</br>
*skinids* - List of definitions for character skin/model identifiers</br>
*textstyle* - List of definitions for GameText styles</br>
*vehids* - List of definitions for all available vehicles</br>
*vehhealth* - Vehicle Health configurations</br>
*carcols* - List of definitions for all available vehicle colors</br>
*paintjob* - List of definitions for all available vehicle paintjobs</br>
*weaponids* - List of definitions for weapon identifiers, sorted by weapon slot IDs</br>
*weatherids* - List of definitions for weather identifiers

# Custom Functions

ISAMPP uses various stock functions which may be useful in creating your custom game modes for SA-MP 
or simply for debugging purposes. These stock functions are defined in *i_sampp.inc* file.

#### isampp_console_printversion()
*Outputs ISAMPP version to server console.*

#### MppTeleport(playerid, locationid)
*Teleports player to desired location passed as parameter ’locationid’.*

#### MppTeleportEx(playerid, locationid, pstringcolor)
*Same as MppTeleport, plus outputs location name to in-game chat window.*

#### MppTeleportToCoords(playerid, x, y, z, interiorid, facingangle)
*Teleports player to specified xyz coordinates, supplied with interior identifier and player facing angle.*

#### MppShowPlayerPosition(playerid, pstringcolor)
*Outputs current player location coordinates, interior identifier, facing angle and player camera position coordinates to in-game chat window.*

#### MppShowVehicleInfo(playerid, vehicleid, pstringcolor)
*Outputs ID, model, health, position and rotation of vehicle in which is player currently sitting to in-game chat window.*
