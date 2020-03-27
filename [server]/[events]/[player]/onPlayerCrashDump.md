### onPlayerCrashDump
```Squirrel
function onPlayerCrashDump( player, crashReport )
```

Called when a player crashes his game. It stores a crash log to your `%appdata$/VCMP/04beta/crashlogs` path.

#### Arguments

- [CPlayer] *player* - player's instance
- [string] *crashReport* - the report of the recent crash

#### Returns
> void
