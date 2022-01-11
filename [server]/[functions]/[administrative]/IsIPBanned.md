### IsIPBanned
```Squirrel
IsIPBanned(ip)
```

Checks if an IP address is banned from the server.

#### Arguments
- [string] *ip* - The IP address to check ban status for.

#### Returns
> true if the IP is banned, false otherwise.

#### Examples
```Squirrel
function onPlayerCommand(player, command, text)
{
    if(command == "checkipbanned")
    {
        if (!text) 
        {
            MessagePlayer("[Syntax] - /checkipbanned <IP>", player);
            return 1;
        }

        if(IsIPBanned) MessagePlayer("The specified IP is banned!", player);
        else MessagePlayer("The specified IP is not banned!", player);
    }
    return 1;
}
```