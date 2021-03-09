## sep.cfg
This repo also holds the latest SEP.cfg (with help from certain members, like kektram and MIKE). Download the latest SEP.cfg and put it into %appdata%\PopstarDevs\2Take1Menu\cfg\  and obviously have windows replace the old file with new file.

## default config
This repo also has a default (2Take1Menu.ini) profile that has all recomended protections/event hooks enabled for you. Download the latest 2Take1Menu.ini and put into %appdata%\PopstarDevs\2Take1Menu\ and replace the old with the new file (this will reset your default profile).

## default config alt
This repo also has a default (2Take1Menu.ini) profile that has all recomended protections/event hooks enabled for you. Download the latest 2Take1Menu.ini and put into %appdata%\PopstarDevs\2Take1Menu\ and replace the old with the new file (this will reset your default profile).
> the alt profile offers keybind options for TKL/60%/80%/90% keyboards.

## Recommended Protections
### Protections
- Disable Background Script  
>    When Rockstar pushes code for your game to execute without an actual update
- Crash - Block & Notify  
>   sync mismatch type 2 sometimes gives false positives, this detection can be disabled at online - modder detection. disable at own risk. (turning the option on, disables this detection)
- Block Script Event Kick
- Block Reports
- Block Crew Kick - Block & Notify
- block collectable drops - Block & Notify
- Block Money Drops - Block & Notify  
>	Doesn't stop you from picking up your own money drops. And may produce False Positives due to other clients trying to sync the pickup entities to you.
- Block Attachments - Block & Notify  
>	May break certain missions, e.g. Casino Heist
- Block Cage Objects - Block & Notify
- Block Clones - Block  
>	Due to entity sync, setting this to Notify, will produce false positives.
- Block Model Changes - Block & Notify
- Notify when Rockstar Admin is present.
- Notify When Someone Is Spectating Me
- Notify when Modder is detected.
- Notify when someone drops cash.  
>	Optional, as this is already in Modder Detection

#### Block from Modders
> When 2take1 detects a modder, it will block the selected things from that person
> strongly recommended to keep this section enabled.

- Block Net Events
- Block Script Events
- Block Global Broadcast
- Block Peds
- Block Objects
- Block Vehicles  
>	This might cause issues, like making the person appear under the map when they in a vehicle.
- Block Pickups  
>	Like money, weapons, health, etc
- Block Automobiles
- Block Bikes
- Block Boats
- Block Doors
- Block Helis
- Block Pickup Placements
- Block Plane
- Block Submarines
- Block Cunts
> people will appear frozen cos of this.
- Block Trailers
- Block Train

### Event Hooks
#### Event Hook logs
- Log script events.  
>	This is optional, and it will fill your log file up a bit. Useful for SEP.cfg and custom lua script creations.
- Log net events.  
>	This is Optional, and it will quickly fill your log file.
- Freemode crash log.  
>	Not really needed anymore, due to "Block Script Event Kicks" protection.

#### Script Events
>	Be sure to grab the latest SEP.cfg from [#script-event-protection-share](https://discord.com/channels/606546434808086529/630443996195586108) or [Releases](https://github.com/Entrodor/2T1-Protex/releases). 
> If you are script host, you will be blocking anything here thats set to Block. which may impact legit players. 

- Invalid Apartment  Invite: Block & Notify
- Apartment Invite: Block & Notify
> disable before doing missions/jobs/heists
- Force Send to Island: Block & Notify
> disable before doing payo cerico heist/beach party
- Invite: Block & Notify
> disable before doing missions/jobs/heists
- CEO Ban/Terminate/Dismiss: Block & Notify
> blocking these will prevent you from being kicked from a ceo youre in, even via legit methods
- Rotate Camera: Block (OPTIONAL)
> dont set to notify, else false positives.
- Block Passive Mode: Block
> haven't tested with notify enabled.
- Remote Blind Eye: ANY (OPTIONAL)
> set to whatever option you want
- CEO 10k Bonus: ANY (OPTIONAL)
- Modded Spectate: Notify (OPTIONAL)
> Block is untested. this will mark person as modder. maybe some false positives?
- Destroy Personal Vehicle: ANY (OPTIONAL)
> untested, dunno what it actually does?
- Kick From Vehicle: Block & Notify
- Vehicle EMP: Block & Notify
> disable during arena war
- Disable Jumping: Block & Notify
- Transaction Fail: Block & Notify
- Show Banner: ANY (OPTIONAL)
- Send Modded Bounty: ANY (OPTIONAL)
> people who have a bounty will also trigger this event.
- Send Bounty: ANY (OPTIONAL)
> people who have a bounty will also trigger this event.
- Sound Spam: ANY
> may interfere with mc/ceo invites
- kick from MC club: ANY (OPTIONAL
> may have false positives? dunno
- Remote OTR: ANY (OPTIONAL)
- Clear Wanted Level: ANY (OPTIONAL)
- Insurance Fraud: Block & Notify
- Police Bribe: ANY (OPTIONAL)
- Script Event Crash: Block & Notify
- Impulse Modder Detection: Notify
- General Bad Events: Block & Notify
> may have false positives
- Notify: Notify (OPTIONAL)
> unknown uses
- UNTESTED
> these events arent fully tested. enable at own discretion.

#### Net Events
>  enable the "disable all net event hooks" option to disable all these, before accessing jobs/missions/etc

- NET CLEAR PED TASKS - Block & Notify
>	May interfere with some jobs/missions
- GAME CLOCK - Block
>	OPTIONAL, 2take1 crash protex blocks invalid time crashes. Enable if you hate people changing time
- GAME WEATHER - Block
>	OPTIONAL, 2take1 crash protex blocks invalid weather crashes. Enable if you hate people changing weather
- NET PTFX - Block or Block & Notify
>	REQUIRED. Impulse uses this to crash you
- FIRE - Block 
>	OPTIONAL
- EXPLOSION - Block & Notify OR Notify only
>	Notify is good for when you  want to know who is blame killing the lobby
- REQUEST CONTROL - Block 
>	Stops modders from fuckin with the vehicle you're currently using
>	Notify is optional, and may be bit spammy
- GIVE WEAPON - Block & Notify
>	OPTIONAL
- REMOVE WEAPON - Block & Notify
>	OPTIONAL
- REMOVE ALL WEAPONS - Block & Notify
>	OPTIONAL
- GIVE PICKUP REWARDS - Notify
>	OPTIONAL. Can be used to detect if someone tries to crash you, but also has legitimate uses in CEO missions
- VOTE KICKS - Notify
>	OPTIONAL. Setting this to block does NOTHING. And the notifications only tell you that the person is vote kicking *someone* not just specifically you

### Notes
- Event Hooks > Net Events > VEHICLE COMPONENT CTRL will stop people from going into vehicles near you

### OPTIONAL
- NET CHECK EXE SIZE - Notify
>	It has been observed that some modders leak this event
- NET CHECK CODE CRCS - Notify
>	It has been observed that some modders leak this event
