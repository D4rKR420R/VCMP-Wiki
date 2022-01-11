### onLoginAttempt
```Squirrel
function onLoginAttempt( playerName, password, ipAddress )
```

Called when a player is attempting to connect to the server.

#### Arguments

- [string] *playerName* - the player's nickname
- [string] *password* - the password he used to connect if the server was locked
- [string] *ipAddress* - the player's IP address

### Returns
> integer - 1 if the player successfully connected to the server, 0 otherwise (it will prevent the player from connecting)
