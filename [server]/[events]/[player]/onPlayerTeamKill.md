### onPlayerTeamKill
```Squirrel
function onPlayerTeamKill( killer, player, weapon, bodypart )
```

Hence similar to `onPlayerKill`, this gets called if the player killed his own team-mate. 

#### Arguments

- [CPlayer] *killer* - the player who killed the victim
- [CPlayer] *player* - the victim
- [integer] *weapon* - what weapon the killer used
- [integer] *bodypart* - where did the killer hit him to his death

#### Returns

> void

#### Example
```Squirrel
// Custom-made enumeration to identify the bodypart
enum BodyPart
{
    Body = 0,
    Torso = 1,
    LeftArm = 2,
    RightArm = 3,
    LeftLeg = 4,
    RightLeg = 5,
    Head = 6,
    InVehicle = 7
}

function GetBodypart( ID ) // Used to return the bodypart as a string
{
    switch( ID )
    {
        case BodyPart.Body:
            return "Body";
        break;
        case BodyPart.Torso:
            return "Torso";
        break;
        case BodyPart.LeftArm:
            return "LeftArm";
        break;
        case BodyPart.RightArm:
            return "Right Arm";
        break;
        case BodyPart.LeftLeg:
            return "Left Leg";
        break;
        case BodyPart.RightLeg:
            return "Right Leg";
        break;
        case BodyPart.Head:
            return "Head";
        break;
        case BodyPart.InVehicle:
            return "Vehicle";
        break; 
    }
}

function onPlayerTeamKill( killer, player, weapon, reason )
{
    // Let's kill the killer for being rude!
    killer.Health = 0; // Kill the killer
    Message( "[#FFFFFF]"+ killer.Name +" was autokilled for killing his own team-mate" );
}
```

As described in the snippet, we're killing the killer by setting his health to zero and outputting a message to everybody using `Message`.
