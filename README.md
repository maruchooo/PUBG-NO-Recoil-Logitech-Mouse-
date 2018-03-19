AT YOUR OWN RISK
logitech gaming software never triggered any banwaves in the past, but this doesn't mean there won't be any banwaves in the future.
ChangeLog
2017.12.23

update for 3.5.5.6 (1.0 release) Script Effect
2017.10.18

Fixed macro disable logic, optimized for tossing grenades
Added hotkey to disable macro named "ignore_key", default to "shift"
2017.10.15

Added sensitivity setting.
2017.10.14

Added uzi and scar-l recoil table.
The default fire button is changed to "pause".
Removed the full attachment mode because the chances of geting all attachments is low, and lacks testing.
Rewriting the logic: now the trigger speed is on par with the weapon firing rate.
How To Use
download and install logitech gaming software[LGS]
http://support.logitech.com/software/lgs
click PUBG in LGS, select Scripting. 
copy and paste script from adv_mode.lua to script box.
Ctrl + S to save.
How to Edit Setting


1. Assign buttons to weapon
you can get the button numbers from logitech log window. When you click a mouse button, the log will prompt event = MOUSE_BUTTON_RELEASED, arg = X, X is the button number.
there are 6 weapon types. if you have a logitech mouse with less than 6 buttons, map unused buttons/weapons to nil.
You should always assign a button to cancel the recoil macro. set_off_key
2. Set the fire key and the mode switch key.
unset the Fire binding in game from your mouse left button, and set it to Pause key. This needs to be consistent between the script and the game setting.
When the mode switch key is pressed, recoil is magnified by 3-4x, consistent with 4x scope mode.
By default in the script , fire key is pause , mode switch key is capslock.
always keep your weapons in single-fire mode. The script will automatically fire in auto mode, including M16A1s


3. Ignore Key (script pause)
You can set a ignore Key, and when the key is pressed, the script pauses.
Limited by LGS, you can only select "lalt", "ralt", "alt" "lshift", "rshift", "shift" "lctrl", "rctrl", "ctrl" and Logitech G Key(Logitech game keyboard only)
By default the ignore key is "lshift"
4. Sensitivity Setting
If you modify the mouse sensitivity settings in the game menu, you need to modify the settings in script.
Mouse dpi does not affect the script. this is built into Logitech driver functionality.


5. Obfs Setting
by default, shoot interval random between 30-39ms. You can modify script variables to change this behavior.

When weapon_speed_mode = true, shots will be fired the same rate as weapon base rate, instead of the above random interval.

6. You should always use Ctrl + S to save script after edit script.
Recommended settings
Logitech's most gaming mice contain 5 shortcuts. The default 1 forward, 1 back, 1 zoom, a reduced dpi, a magnifying glass.

Assign a button to use ump9, so that the keys are also suitable for full accessory m416 and scar-l.
Assign a button to use m16a1, m16a1 with red dot sight or holographic sight, do not need other accessories, you can play a power.
Assign a button using akm, akm mode also applies to sks and mini 14.
Assign a button to use a big jump.
Assign a button to cancel the no-recoil.


Not working?
run LGS as administrator
UAC will isolate user32.dll‘s function between users and administrators. both keybd_event and SendInput function are in user32.dll. so if you run pubg as administrator , you also need to run LGS as administrator.

You may not notice that pubg in the admin, may be pubg is child process of steam.exe , and steam is child process of steam update , steam update must run as admin.

set "Lock profile while game is running"
By default ， LGS will only run profile when game's window is "active", use GetActiveWindow , but in windows 10 , input and notification will often become active window, maybe bug maybe not.

Copyright
The Unlicense
No support, for suggestions, use Issues.
