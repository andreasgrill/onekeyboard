onekeyboard
===========
## Does it work?
Actually it works pretty well. 

 * Textfield navigation (⌥ + Left, `⌘ + Shift + Left`, ...)
 * Copy&Paste (`⌘ + C`, `⌘ + X`, `⌘ + V`)
 * Symbols (`@`, `[](){}/|`, ...)
 * Windows key is still accessible through CTRL (`^`)

## How to get it working
### Requirements
 * [autohotkey](http://www.autohotkey.com/) - lightweight program to interpret customized hotkeys.
 * mac.ahk script to correctly map the hotkeys (e.g. the script that does all the work).
 * Some customization to swap the CMD (`⌘`) and the CTRL (`^`) keys lowlevel (see the following paragraph).
 * German keyboard layout (or you probably need to adjust the mac.ahk script for your language).


### How-To
At first we have swap the CMD (`⌘`) key with the CTRL (`^`) key. This is something that we shouldn't do with autohotkey, because it is more reliable to change such an important key on a lower level. There are multiple options to achieve this:

 * If you are using Windows through a VM such as Parallels Desktop, you could swap the keys by using the Parallels shortcut settings ([Example](images/parallels.png)).
 * You could swap the keys by mapping them through the registry by applying the ctrlswap.reg file.
 * You could also use a free program to swap the keys (such as KeyTweak) but it produces the same registry entry anyway.


After you have successfully swapped the two keys, you just need to install autohotkey and start the mac.ahk script.
If you don't use a German keyboard layout, you probably want to adjust the mac.ahk script to map special characters (such as `[](){}?@<>`) to the correct position. You are welcome to do so and create a pull request :)
