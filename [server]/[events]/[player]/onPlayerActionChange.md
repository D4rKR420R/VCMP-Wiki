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
        case pActions.None:
            cond = "none";
        break;
        case pActions.Normal:
            cond = "normal";
        break;
        case pActions.Aiming:   
            cond = "aiming";
        break;
        case pActions.Shooting:
            cond = "shooting";
        break;
        case pActions.Jumping:
            cond = "jumping";
        break;
        case pActions.OnGround:
            cond = "lying on the ground";
        break;
        case pActions.GettingUp:
            cond = "getting up";
        break;
        case pActions.JumpingFromVeh:
            cond = "jumping from vehicle";
        break;
        case pActions.Driving:
            cond = "driving";
        break;
        case pActions.Drying:
            cond = "dying";
        break;
        case pActions.Wasted:
            cond = "wasted";
        break;
        case pActions.EnteringVeh:
            cond = "entering a vehicle";
        break;
        case pActions.ExitingVeh:
            cond = "exiting a vehicle";
        break;
    }
    // Send a message to the server
    Message( "[#FFFFFF]"+ player.Name +"'s current action: "+ cond );
}
```

As you can see, we declared a lovely enumeration to identify the action using the action ID (`newAction`) and we then outputted it using the `Message` function.
