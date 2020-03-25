### onPlayerPart
```Squirrel
function onPlayerPart( player, reason )
```

Called when a player leaves the server.

#### Arguments

- [CPlayer] *player*
- [integer] *reason*

#### Returns

> void

#### Example
```Squirrel
// Custom-made enumeration
enum PartReason
{
    Timeout = 0,
    Quit = 1,
    Kick = 2,
    Crash = 3,
    AntiCheat = 4
}

function onPlayerPart( player, reason )
{
    local msg = ""; // Define variable to store the message
    switch( reason )
    {
        case PartReason.Timeout:
            msg = "timeout";
        break;
        case PartReason.Quit:
            msg = "quit";
        break;
        case PartReason.Kick:
            msg = "kicked";
        break;
        case PartReason.Crash:
            msg = "crashed";
        break;
        case PartReason.AntiCheat:
            msg = "anti-cheat";
        break;
    }
    Message( "[#FFFFFF]"+ player.Name +" disconnected ["+ msg +"]." ); // Output message
}
```

It will message the whole server that a player left the server with a reason using `Message` and our custom-made enumeration, `PartReason`, to identify the reason.
