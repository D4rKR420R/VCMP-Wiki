### onClientScriptData
```Squirrel
function onClientScriptData( player, stream )
```

Called when the client-side sends data to the server-side.

#### Arguments

- [CPlayer] *player*
- [CStream] *stream*

#### Returns
> void

#### Example
`store/script/main.nut`
```Squirrel
function SendStringToServer()
{
    local data = Stream();
    data.WriteByte( 0x01 );
    data.WriteString( "Hi, server-side!" );
    Server.SendData( data );
}

SendStringToServer();
```
`script/main.nut`
```Squirrel
function onClientScriptData( player, stream )
{
    local byte = stream.ReadByte();
    switch( byte )
    {
        case 0x01:
            local message = stream.ReadString();
            if( message ) print( message );
        break;
    }
}
```

The client-side will send this message to the server-side, where the `onClientScriptData` will fetch that stream.

> :warning: NOTE: If you're be writting bytes, it should written first before any other data type to function properly.