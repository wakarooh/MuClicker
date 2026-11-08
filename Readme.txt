# MuClicker
AutoClicker for MU Online Game Build (Mu Helper)
If you like my program, please donate: https://paypal.me/RayAnthonyLeong

1. Target detection​
- Auto-search: It scans for play.exe every 500 ms.
- Locked options: Every setting is greyed out until the process is found, and they unlock on their own once it appears.
- Status label: It shows “Searching...”, “Found”, or “Found (minimized)” in orange or green.
- Window recovery: If the game closes, the clicker stops and goes back to searching. If the process stays alive but its window is recreated (a relog, say), it finds the new window.
- Single instance: A mutex stops two copies from running, because they would fight over the F6 and F7 hotkeys

2. Click options​
- Mouse button: Left or right click.
- Double click: An optional checkbox.
- Interval: Time between clicks in milliseconds. 100 ms is 10 clicks per second, and the minimum is 1.
- Random ±ms: Adds jitter to each interval so the timing is less uniform.
- Stop after N clicks: 0 means it never stops.

4. Fake window focus​
- Is an optional extra for the background methods. It posts activate and focus messages so the game thinks it is the active window, then un-focuses it afterward. It is meant for games that ignore clicks when they are in the background.

5. Click position​
- Capture with F7: Hover over a spot in the game and press F7.
- Default: With no capture, it clicks the center of the game window.
- Reset: Pressing F7 with the cursor outside the game resets to center.
- Minimized windows: A minimized window reports a 0×0 size, so it uses the last known size. If it has never seen the window restored, it works the size out from the window’s stored position.

6. Controls​
- F6 starts and stops. The Start/Stop button does the same.
- F7 captures the click position.
- Closing: The program only closes through the X button, which prevents accidental exits.

7. Status and feedback​
- It shows a live click counter, refreshed every 250 ms to avoid flicker.
- It adds notes such as “game minimized - clicking in background”.
- It shows the total click count when stopped, including when the game closes.

8. Extras​
- Run as administrator: #RequireAdmin is needed so it can send input to a game that runs elevated.
- 32-bit build: UseX64=n compiles it as 32-bit.
- Things to note​
- Game rules: The help text itself warns that auto clickers may violate the game’s rules, and background-click tools like this are the kind many anti-cheat systems flag.

This was supposedly for InfinityMU Only but one of the staff named Nikki accused me that I stole the code which originally I am the one who wrote the code in AutoIt. 
