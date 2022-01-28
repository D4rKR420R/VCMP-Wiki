### Server::ServerData
```Squirrel
function Server::ServerData(stream)
```

Called when some data is received from the server.

#### Arguments
- [Stream] *stream* - The data stream received.

#### Returns
> void

#### Example
`store/script/main.nut`
```Squirrel
enum StreamType
{
    ServerName = 0x01
}   

function Server::ServerData(stream)
{
    local Type = stream.ReadByte();
    switch(Type)
    {
        case StreamType.ServerName:
            Console.Print("Welcome to " + stream.ReadString());
            break;
    }
}
```

`script/main.nut`
```Squirrel
enum StreamType
{
    ServerName = 0x01
}

function onPlayerCommand(player, command, text)
{
    if(command == "clientgreet")
    {
        Stream.WriteByte(StreamType.ServerName);
        Stream.WriteString(GetServerName());
        Stream.SendStream(player);
    }
    return 1;
}
```

> :warning: NOTE: If you're be writting bytes, it should written first before any other data type to function properly.