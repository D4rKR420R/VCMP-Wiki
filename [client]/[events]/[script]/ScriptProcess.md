### Script::ScriptProcess
```Squirrel
function Script::ScriptProcess()
```

Called once every frame.

> :warning: NOTE: Computationally expensive operations in this event may cause lagging.

#### Arguments
- None

#### Returns
> void

#### Example
```Squirrel
last_checked <- Script.GetTicks(); fps <- 0;

function Script::ScriptProcess()
{
    if(Script.GetTicks() - last_checked >= 1000)
    {
        ::last_checked = Script.GetTicks();
        Console.Print("Your FPS: " + fps);

        ::fps = 0;
    }

    ::fps++;
}
```