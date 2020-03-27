### onPlayerStateChange
```Squirrel
function onPlayerStateChange( player, oldState, newState )
```

Called when a player's state changed.

#### Arguments

- [CPlayer] *player* - player's instance
- [integer] *oldState* - previous state ID
- [integer] *newState* - latest state ID

#### Returns
> void

#### Example
```Squirrel
// Custom-made enumeration to identify the state
enum pState
{
    None = 0,
	Normal = 1,
	Aim = 2,
	Driver = 3,
	Passenger = 4,
	EnterDriver = 5,
	EnterPassenger = 6,
	Exit = 7,
    Unspawned = 8
}

function onPlayerStateChange( player, oldState, newState )
{
    local state = ""; // Define variable to store the state
    switch( newState )
    {
        case pState.None:
            state = "none";
        break;
        case pState.Normal:
            state = "normal"
        break;
        case pState.Aim:
            state = "aiming";
        break;
        case pState.Driver:
            state = "driver";
        break;
        case pState.Passenger:
            state = "passenger";
        break;
        case pState.EnterDriver:
            state = "entering as driver";
        break;
        case pState.EnterPassenger:
            state = "entering as passenger";
        break;
        case pState.Exit:
            state = "exiting vehicle";
        break;
        case pState.Unspawned:
            state = "unspawned";
        break;
    }
    Message( "[#FFFFFF]"+ player.Name +"s current state: "+ state );
}
```

In this example, we outputted a message using the `Message` function to determine his current state.
