# Mario's Max3

## Who's it for?

Have an additional 2K/3K/4K monitor which can be rotated in 4 directions? If you are a programmer, especially when you are a frontend developer always put the browser in one monitor, with the developer's tool and source editor in another, you'll find it's hard to sufficiently use the monitor no matter how it's oriented.

In my way, I rotate my Monitor II vertically and place the developer's tool and source editor in it in horizontal rows.

In handy Max3, some frequently used hotkeys are defined. To place the said windows is totally effortless.

Hotkey | Effect
--- | ---
Win + Numpad 8 | Place the active window into the top part of three
Win + Numpad 5 | Place the active window into the middle part of three
Win + Numpad 2 | Place the active window into the bottom part of three
Win + Numpad 4 | Place the active window into the left monitor and maximize it `*`
Win + Numpad 6 | Place the active window into the right monitor and maximize it `*`

`*` Supposing you place your Monitor II in the right.

If you are facing the same situation as I am, you should try it.

## Why so called?

There's a charged tool called MaxTo. Max3 is simple but open sourced. And it split a monitor into three, so Max3 it's called.

## Want customization?

Max3 is written in [AutoHotkey](http://www.autohotkey.com) script. If you want to customize Max3, such as to change the hotkeys or to alter the position parameters, you should first go to AutoHotkey official site to have some common concepts of AutoHotKey. Then read and modify the source script to make it your own.

Some explaination for the script:

* X, Y0, Y1, Y2, W, H
  
  The variables store three windows positions. Any placed window will be W * H sized. If it's placed top, it will be placed at (X, Y0), centered - (X, Y1) and bottom - (X, Y2). The values will be saved into system registry. You may create more variables and save them into system registry if you want to split your monitor into more parts or have more monitors to split.
  
* Mario's Max3 - Monitor Locator

  It's a window for you to locate the monitor you want to split. If you have more monitors to split, you ought to get the monitor list and add some radio buttons to indicate which one you want to split.

* ButtonOK
  
  This will be used to save the coordinates into system registry. If you want to split your monitor into more parts or have more than one virtical monitor and want to split, use the radio buttons to have the coordinates saved to variables which can be distinguished. For example, hard coded X_1, Y0_1, Y1_1, Y2_1, W1, H1 for monitor 1 and X_2, Y0_2, Y1_2, Y2_2, W2, H2 for monitor 2.

* Hotkeys

  Registered hotkeys will move the current window to designated position with width and height set. Add as many hotkeys as you want with different WinMove parameters.

## Virus alert?

According to [virustotal](https://www.virustotal.com/en/file/fc00c1584c4371e9331a19a5795600178a85236e88e9974aeca87aeaba637a2c/analysis/1459478515/), 4 out of 56 antivirus programs reported Max3.exe as devil. If you suspect it, please compile your own excutable with AutoHotkey. Since the original binary file of AutoHotkey hasn't the sepcified SysTray menu icons, please remove all the icon statements in the script.

The statements look like this:

```
  Menu, Tray, Icon, 1&, %A_ScriptFullPath%, -997, 64
```

Otherwise, icons can be added to your compiled executable by using a utility such as [Resource Hacker](http://angusj.com/resourcehacker/) (freeware) to edit it.

## Misc

* Ctrl+T for Git Bash if it's installed. When hit Ctrl+T in a Git Bash window which is __not__ in the / folder, a new Git Bash window will be opened and switched to the same path.
* Win+A for AutoHotkey Help if AutoHotkey is installed.

## License

MIT
