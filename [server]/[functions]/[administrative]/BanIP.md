### BanIP
```Squirrel
BanIP(ip)
```

Bans an IP address from the server.

#### Arguments
- [string] *ip* - The IP address to be banned.

#### Returns
> void

#### Examples
```Squirrel
function onPlayerCommand(player, command, text)
{
    if(command == "banip")
    {
        if (!text) 
        {
            MessagePlayer("[Syntax] - /banip <IP>", player);
            return 1;
        }

        BanIP(text);
    }
    return 1;
}
```