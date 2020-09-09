Original plugin developed by DarkunderdoG (http://tshock.co/xf/index.php?threads/1-15-afk-warp-kick-plugin.2594/)

When a player is idle/AFK for a defined time, the server will warp the player to the "afk" warp or when the player types `/afk`.

Commands
-------
* `/afk` - warps the user to afk
* `/afktime` - provides the player details about their afk status
* `/return` - warps the player back to their original position (Talking or leaving the afk region also does this)
* `/afkwarptime <seconds>` Temporarily changes the duration of when a player is warped to afk
* `/afkkicktime <seconds>` - Temporarily changes the duration of when a player is kicked from being afk
* `/afkreload` - reloads the AFK config file

Config File (AFKconfig.json)
-------
```
{
  "afkwarp": true, <---Enable/Disable warp players to afk
  "afkkick": false, <---Enable/Disable kick players in afk
  "afkwarptime": 300, <---Duration in seconds before being warped to afk
  "afkkicktime": 700, <---Duration in seconds before being kicked
  "afkspam": 20, <--Delay in seconds before the player can use /afk again
  "awayMessage": "{player} is away.", <--Broadcasted message when player is afk
  "returnMessage": "{player} is no longer afk." <--Broadcasted message when player returns
}
```

Usage
-----
For AFK Warp:
  Create a region called "afk".
  Create a warp called "afk" within the afk region.
  To hide the warp from the warp list:
  `/warp hide afk true`
  
  Now users can use `/afk`

For AFK Kick:
  No setup required other than to have it enabled. It will warn players 3 times before kicking them. (at 70%, 80%, and 90% of the afkkicktime)
  Give user groups `afk.nokick` permission to prevent them from being kicked.
