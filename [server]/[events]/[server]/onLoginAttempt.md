### onLoginAttempt
```Squirrel
function onLoginAttempt( playerName, password, ipAddress )
```

Called a player is attempting to connect to the server.

#### Arguments

- [string] *playerName*
- [string] *password*
- [string] *ipAddress*

### Returns
> Integer - 1 if the player successfully connected to the server, 0 otherwise (it will prevent the player from connecting)
