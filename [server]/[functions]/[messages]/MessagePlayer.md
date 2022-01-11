### MessagePlayer
```Squirrel
MessagePlayer(message, player)
```

Sends a message to a specific player.

#### Arguments
- [string] *message* - The message to be sent.
- [CPlayer] *player* - The player to send the message to.

#### Returns
> void

#### Examples
```Squirrel
function onPlayerCommand(player, command, text)
{
    if(command == "cash")
    {
        MessagePlayer("You have " + player.Cash + " cash.", player);
    }

    return 1;
}
```

> Hexadecimal color codes can be used to color the message string, enclosed with square brackets.