### MessageAllExcept
```Squirrel
MessageAllExcept(message, player)
```

Sends a message to all players in the server, except one.

#### Arguments
- [string] *message* - The message to be sent.
- [CPlayer] *player* - The player to exclude the message from.

#### Returns
> void

#### Examples
```Squirrel
function onPlayerCommand(player, command, text)
{
	if(command == "msg")
	{
		MessageAllExcept("Hello all except myself, have fun here!", player);
	}
	return 1;
}
```

> Hexadecimal color codes can be used to color the message string, enclosed with square brackets.