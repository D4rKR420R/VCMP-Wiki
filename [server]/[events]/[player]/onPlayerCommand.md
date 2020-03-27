### onPlayerCommand
``` Squirrel
function onPlayerCommand( player, command, text )
```

Called when a player enters a command using the in-built command system prefix, `/`. The system takes care of multiple arguments from `text`; it's up to you to separate those arguments.

> :warning: NOTE: `command` stores the name of the command without the prefix (`/`).

> :warning: NOTE: To overwrite the in-built command system with your own prefix, you can try slicing the message from the `onPlayerChat` callback and run your own command function.

#### Arguments

- [CPlayer] *player* - player's instance
- [string] *command* - the command
- [string] *text* - the arguments after the command

#### Returns
> integer - 1 if the player entered a command, 0 otherwise

#### Example
```Squirrel
function onPlayerCommand( player, command, text )
{
    // Highly recommend setting the text lowercase
    local cmd = command.tolower();
    switch( cmd )
    {
        // Check if the command exists
        case "healme":
            // Check if the player's health is already 100HP
            if( player.Health != 100 ) return MessagePlayer( "[#FFFFFF][ERROR] You already have max health.", player );
            else player.Health = 100;
        break;
        case "killhim":
            // Check for arguments
            if( !text ) return MessagePlayer( "[#FFFFFF][ERROR] Use /"+ cmd +" <player>", player );
            local plr = FindPlayer( text ); // Find the player using the arguments
            // Check if he's online
            if( !plr ) return MessagePlayer( "[#FFFFFF][ERROR] Unknown player.", player );
            else plr.Health = 0;
        break;
        // Else, we'll output an error
        default: return MessagePlayer( "[#FFFFFF][ERROR] Unknown command.", player );
    }
    return 1;
}
```

In the first example (the `healme` command), we used a conditional statement to verify if the player already has 100HP. The next example (the `killhim` command), we also used conditional statements to prevent any errors within the code and outputted the warnings using the `MessagePlayer` function to send a message directly to a specific player.