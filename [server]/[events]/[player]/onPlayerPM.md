### onPlayerPM
```Squirrel
function onPlayerPM( sender, recipient, message )
```

Called when a player sends a private message directly to another player using the VC:MP in-built command, `/msg`.

#### Arguments

- [CPlayer] *sender* - the player who sent the private message
- [CPlayer] *recipient* - the player who received the sender's message
- [string] *message* - the message

#### Returns
> integer - 1 if the message was sent successfully, 0 otherwise

#### Example
```Squirrel
function onPlayerPM( sender, recipient, message )
{
    if( !message ) return MessagePlayer( "[#9999ff] Use /msg <player ID> <message>", player );
    MessagePlayer( "[#9999ff] You have a message from "+ sender.Name +": "+ message, recipient );
    MessagePlayer( "[#9999ff] Message successfully sent.", sender );
    return 0; // Exploit the in-built PM system
}
```

*Bam!* We became creative and customized our own private message system, using the `MessagePlayer` function to send the message directly to the sender & recipient.