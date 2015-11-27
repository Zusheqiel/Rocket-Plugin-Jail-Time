#Notice 
This is a fork of JailTime by ApokPT (https://github.com/ApokPT) and is hobby to better learn C# and API development for Rocket.

The plugin is working with Rocket 4.6.4.0+ but I cannot guarantee 100% of this plugint to be working (yet).

### >> All of this is a Work-in-Progress. :) <<

# JailTime
### Send players to jail

JailTime allows the caller to create Jail Cells and place players in them. Players in Jail Cells cannot move more then X yards from the cell and will die/teleport back to the cell if they move too far (disconnect and suicide will also teleport you back to the cell).

You also have the option to define if a Jailed player is banned for X seconds if he decides to disconnect while in jail.

## Available Commands
Command | Action
------- | -------
/jail set <cell>				 | creates a cell at callers location
/jail unset <cell>				 | deletes the cell
/jail list cells				 | show the list of created cells
/jail list players				 | show the list of arrested players
/jail add <player> <time> <cell> | add a player to <cell> for <time> seconds (if a <cell> is not defined, it will choose a random one; if <time> is not defined it will use default config time)
/jail remove <player>			 | remove a player from jail
/jail t <cell>				     | teleport caller to cell

## Available Permissions
Permission | Action
------- | -------
<Command>jail</Command>			| allow caller to set/unset/list cells and add/remove/list players
<Command>jail.immune</Command>	| target is immune to jail (admin has this by default)

## Other Options
Option | Action
------- | -------
KillInsteadOfTeleport			| Kill player that move away from the cell instead of teleporting them.
BanOnReconnect					| Ban player that reconnects while in jail.
BanOnReconnectTime				| Time for ban on reconnect (set 0 for permanent)
WalkDistance					| Maximum distance a player can move from the cell center
JailTimeInSeconds 				| Default arrest time if no time is specified