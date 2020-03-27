### onPlayerModuleList
```Squirrel
function onPlayerModuleList( player, moduleList )
```

Called when a player requests for another player's module list. It get a list of loaded modules (i.e. DLLs) on a player's game without crashing the client. In addition, this callback receives that list and parses it.

#### Arguments

- [CPlayer] *player* - player's instance
- [string] *moduleList* - the list of loaded modules

#### Returns
> void

#### Example
`Snippet made by "rww"`
```Squirrel
function onPlayerModuleList(player,string)
{
    Logs("Modules/"+player.IP+".txt","[PLAYER PLUGINS] ["+GetRealTime()+"] ["+player.ID+"] [ "+player.Name+" ] IP: [ "+player.IP+" ] UID: [ "+player.UniqueID+" ] UID2: [ "+player.UniqueID2+" ] \n"+s);
    print("[PLAYER PLUGINS] ["+GetRealTime()+"] ["+player.ID+"] [ "+player.Name+" ] IP: [ "+player.IP+" ] UID: [ "+player.UniqueID+" ] UID2: [ "+player.UniqueID2+" ] \n"+s);
    return 1;
}

function onPlayerCommand(player,cmd,text)
{
    if (cmd) cmd = cmd.tolower();
    local plr, veh = player.Vehicle;
    if (text) plr = GetPlayer(text);
    if (cmd == "getmodules" || cmd == "getplugins" || cmd == "getasi")
    {
    if (!text) ClientMessage("* Type: [#ffaa00]/"+cmd+" [Player ID]!",player,255,30,30,255);
    else if (!plr) ClientMessage("* This player doesn't exist!",player,255,30,30,255);
    else plr.RequestModuleList();
    }
    else ClientMessage("* This command doesn't exist!",player,255,30,30,255);
    return 1;
}

function GetPlayer(plr)
{
 if (plr)
 {
  if (IsNum(plr))
  {
   plr = FindPlayer(plr.tointeger());
   if (plr) return plr;
   else return 0;
  }
  else 
  {
   plr = FindPlayer(plr);
   if (plr) return plr;
   else return 0;
  }
 }
 else return 0;
}

function GetRealTime()
{
    local t = date(time());
    return format(@"%.2d/%.2d/%d - %.2d:%.2d:%.2d", t.day, t.month += 1, t.year, t.hour, t.min, t.sec);
}

function Logs(f,t)
{
 local a = file(f,"a+");
 foreach(char in t)
 a.writen(char,'c'); 
 a.writen('\n','c');
 a = null;
}
```
Kudos for him :wink:! For more information, click [here](https://forum.vc-mp.org/?topic=5891.msg41012#msg41012).