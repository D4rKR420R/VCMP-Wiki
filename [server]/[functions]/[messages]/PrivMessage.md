### PrivMessage
```Squirrel
PrivMessage(player, message)
```

Sends a personal message to a specific player.

#### Arguments
- [CPlayer] *player* - The player to send the message to.
- [string] *message* - The message to be sent.

#### Returns
> void

#### Examples
```Squirrel
function onPlayerCommand(player, command, text)
{
	if(command == "privatemsg")
	{
		PrivMessage(player, "Hey you, have fun here!");
	}
	return 1;
}
```