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
>	Be sure to grab the latest SEP.cfg from [#script-event-protection-share](https://discord.com/channels/606546434808086529/630443996195586108). 
> Please note: You must turn off any script event hook that mentions "mission" or "invite" to access heists, missions, jobs, etc.
> If you are script host, you will be blocking anything here thats set to Block. which may impact legit players. 

- Force to Mission: Block & Notify
- Invite: Block & Notify
- Rotate Camera: Block
> Notify will give false positives when players leave.
- Remote Blind Eye: Block & Notify - OPTIONAL
> if someone else has this effect avtive and they get in your car, youll be notified. 
- CEO 10k Bonus: Block & Notify - OPTIONAL
- Destroy PErsonal Vehicle: Block - OPTIONAL
> honestly, no clue what this actually does...
- kick from vehicle: block & notify
- vehicle EMP: block & notify
> turn this off in Arena War jobs/missions
- Transaction Fail: Block & Notify
- Show Banner: Block / Block & Notify
- Bounty: Block
> setting to notify, will also give you notifications when other players get a bounty, this is a "Broadcast" event
- Off the Radar: Block & Notify - OPTIONAL
- CEO Ban/CEO terminate/CEO dismiss: Block & Notify
> this will actually prevent you from being kicked from a CEO and may stop you from leaving a CEO
- Clear Wanted Level: Block & Notify - OPTIONAL
- Apartment Invite: Block & Notify
- Invalid Apartment Invite: Block & Notify
- Crash Protections: Block & Notify
> Marks the sender as modder. these are script events with bad args which will cause crashes
- Kick Notifications: Notify
> due to "Block Script Event Kicks" setting this to block is useless. this will also automatically mark senders as modders


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
