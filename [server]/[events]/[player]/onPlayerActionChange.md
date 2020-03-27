### onPlayerActionChange
```Squirrel
function onPlayerActionChange( player, oldAction, newAction )
```

Called when the player's action update.

#### Arguments

- [CPlayer] *player* - player's instance
- [integer] *oldAction* - the previous action ID
- [integer] *newAction* - the latest action ID

#### Returns
> void

#### Example
```Squirrel
// Create an enumeration to identify each action ID
enum pActions
{
    None = 0,
    Normal = 1,
    Aiming = 2,
    Shooting = 16,
    Jumping = 41,
    OnGround = 42,
    GettingUp = 43,
    JumpingFromVeh = 44,
    Driving = 50,
    Dying = 54,
    Wasted = 55,
    EnteringVeh = 58,
    ExitingVeh = 60
}

function onPlayerActionChange( player, oldAction, newAction )
{
    local cond = ""; // Define variable to store the condition
    switch( newAction )
    {
        case pAction.None:
            cond = "none";
        break;
        case pAction.Normal:
            cond = "normal";
        break;
        case pAction.Aiming:   
            cond = "aiming";
        break;
        case pAction.Shooting:
            cond = "shooting";
        break;
        case pAction.Jumping:
            cond = "jumping";
        break;
        case pAction.OnGround:
            cond = "lying on the ground";
        break;
        case pAction.GettingUp:
            cond = "getting up";
        break;
        case pAction.JumpingFromVeh:
            cond = "jumping from vehicle";
        break;
        case pAction.Driving:
            cond = "driving";
        break;
        case pAction.Drying:
            cond = "dying";
        break;
        case pAction.Wasted:
            cond = "wasted";
        break;
        case pAction.EnteringVeh:
            cond = "entering a vehicle";
        break;
        case pAction.ExitingVeh:
            cond = "exiting a vehicle";
        break;
    }
    // Send a message to the server
    Message( "[#FFFFFF]"+ player.Name +"'s current action: "+ cond );
}
```

As you can see, we declared a lovely enumeration to identify the action using the action ID (`newAction`) and we then outputted it using the `Message` function.
