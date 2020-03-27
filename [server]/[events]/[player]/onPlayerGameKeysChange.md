### onPlayerGameKeysChange
```Squirrel
function onPlayerGameKeysChange( player, oldKeys, newKeys )
```

Called when a player presses keys.

> :warning: NOTE: Some keys will not trigger this callback.

#### Arguments

- [CPlayer] *player* - player's instance
- [integer] *oldKeys* - previous key pressed
- [integer] *newKeys* - latest key pressed

#### Returns
> void

#### Example
`Snippet made by "Gudio"`
```Squirrel
onfoot <- [ KEY_ONFOOT_FORWARD, KEY_ONFOOT_BACKWARD, KEY_ONFOOT_LEFT, KEY_ONFOOT_RIGHT, KEY_ONFOOT_JUMP, KEY_ONFOOT_SPRINT, KEY_ONFOOT_FIRE, KEY_ONFOOT_CROUCH, KEY_ONFOOT_PUNCH, KEY_ONFOOT_PREVWEP, KEY_ONFOOT_NEXTWEP, KEY_ONFOOT_AIM ];
incar <- [ KEY_INCAR_LEFT, KEY_INCAR_RIGHT, KEY_INCAR_BACKWARD, KEY_INCAR_FORWARD, KEY_INCAR_HORN, KEY_INCAR_LEANUP, KEY_INCAR_LEANDOWN, KEY_INCAR_LOOKLEFT, KEY_INCAR_LOOKRIGHT ];


function getPressedKeys( keysFlag, isOnFoot )
{
 local table, pressedKeys = {}, i = 0;


 if ( isOnFoot )
  table = onfoot;
 else
  table = incar;


 foreach ( key in table )
 {
  if ( key <= keysFlag )
  {
   pressedKeys.rawset( i++, key );
   keysFlag -= key;
  }
 }


 return pressedKeys;
}
```

Check him out [here]( https://forum.vc-mp.org/?topic=215.msg1135#msg1135 )!
