### PrivMessageAll
```Squirrel
PrivMessageAll(player, message)
```

Sends a personal message to a all players in the server.

#### Arguments
- [string] *message* - The message to be sent.

#### Returns
> void

#### Examples
```Squirrel
function onPlayerCommand(player, cmd, text)
{
	if(cmd == "privmsgtoall")
 	{
  		PrivMessageAll("Hey all, have fun here!");
 	}
}
```