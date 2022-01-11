### UnbanIP
```Squirrel
UnbanIP(ip)
```

Unbans an IP address from the server.

#### Arguments
- [string] *ip* - The IP address to be unbanned.

#### Returns
> void

#### Examples
```Squirrel
function onPlayerCommand(player, command, text)
{
    if(command == "unbanip")
    {
        if (!text) 
        {
            MessagePlayer("[Syntax] - /unbanip <IP>", player);
            return 1;
        }

        UnbanIP(text);
    }
    return 1;
}
```