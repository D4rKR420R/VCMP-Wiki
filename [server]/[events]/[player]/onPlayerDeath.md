### onPlayerDeath
```Squirrel
function onPlayerDeath( player, reason )
```

Called when a player dies.

> :warning: NOTE: This callback is only called if the server wasn't able to identify any killer. Specifically, dead from fire, suffocation, etc.

#### Arguments

- [CPlayer] *player*
- [integer] *reason*

#### Returns

> integer - 1 if the player died, 0 otherwise

#### Example
```Squirrel
// Custom-made enumeration
enum DeathReason
{
    Vehicle = 39,
    Explosion = 41,
    Drowned = 43,
    Fell = 44,
    Suicide = 70
}

function onPlayerDeath( player, reason )
{
    local msg = ""; // Definte variable to store the message
    switch( reason )
    {
        case DeathReason.Vehicle:
            msg = "vehicle";
        break;
        case DeathReason.Explosion:
            msg = "explosion";
        break;
        case DeathReason.Drowned:
            msg = "drowned";
        break;
        case DeathReason.Fell:
            msg = "fell to his death";
        break;
        case DeathReason.Suicide:
            msg = "kermit suicide"; // :P
        break;
    }
    Message( "[#FFFFFF]"+ player.Name +" died ["+ msg +"]." ); // Output message
}
```

It will message the whole server that a player died with a reason using `Message` and our custom-made enumeration, `DeathReason`, to identify the reason.