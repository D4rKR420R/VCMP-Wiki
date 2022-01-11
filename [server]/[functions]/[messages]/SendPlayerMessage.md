### SendPlayerMessage
```Squirrel
SendPlayerMessage(playerFrom, playerTo, message)
```

Sends a fake private message from a player to another.

> :warning: The fake private message is not identical to actual private message, the appearance seems to be outdated.

#### Arguments
- [CPlayer] *playerFrom* - The player to send the private message as/from.
- [CPlayer] *playerTo* - The player to send the private message to.
- [string] *message* - The message to be sent.

#### Returns
> void

#### Examples
```Squirrel
function onPlayerKill(killer, player, reason, bodypart)
{
	SendPlayerMessage(killer, player, "hahaha, begginer I killed you.");
	return 1;
}
```