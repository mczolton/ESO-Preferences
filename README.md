# Elder Scrolls Online User Preferences

Preferences location: `%USERPROFILE%\Documents\Elder Scrolls Online\live`

Everybody:
Go to Documents\Elder Scrolls Online\live and open UserSettings.txt and apply these changes:
SET RequestedNumWorkerThreads "-1" to 0.
Stops multithreading stutter. Keep Job threads at -1 otherwise multithreading is completely disabled.
Delete ShaderCache.cooked file.
This gets bloated after changing your shadow settings, etc. The game will rebuild it with your current settings (expect a long initial load time while it rebuilds). This fixed shadows being delayed for me at Character Select screen after changing my settings too many times. File was at 25mb, now it's 6mb.
AMD Crossfire Users:
Tick the check box to allow Crossfire in games with no application profile.
Set crossfire profile to Optimize 1x1
SET PreferExclusiveFullscreen "1"
SET GraphicsDriver.7 "D3D11" - MUST be D3D11 for Crossfire to work. Exclusive Fullscreen doesn't seem to work properly in D3D9.
You should gain at least 50% scaling with efficient GPU usage. AFR mode has same FPS but with 99% usage. With this profile I was sitting at 45% usage on my cards, allowing me to put the rest of the unused usage in downsampling 4K at the same FPS.
8GB + Ram Users:
Apply the LargePage tweak.
Utility:
http://www.mediafire.com/download/aiudd2j3at03j12/LargePage_util.zip
Sources:
http://forums.guru3d.com/showthread.php?t=389072
http://forums.bistudio.com/showthread.php?177454-a-simple-registry-tweak-for-increased-performance
Run the Utility in Admin mode. Add eso.exe (and all your other game's exes). Click save. Apply the registry file that it spits out. Run eso.exe as Admin. Admin is required for Large Page memory region so if you want anything to interact with the game (recorders, monitoring overlays, etc) then you need to run those as Admin too.
This tweak will fix hitching or frametime variance for texture-streaming, camera panning, full 90 degree turns, sudden explosions, etc in most games. This should help in Cyrodiil when 50 players come within draw distance and need to be rendered all at once.
This tweak removed all texture-streaming related 'hitching' for me in Skyrim, Bioshock Infinite, GTA IV and DayZ and helped quite a bit in Watch Dogs.
I have absolutely zero hitching or stutter in ESO now. FPS still drops from the 90-100 region to the 40-60 region in CPU-bound areas (cities, cyrodiil) but that can't be fixed with any system or tweak.
The Obvious:
Set Power Profile to High Performance.
This makes your CPU clock run at full speed and on Windows 8 it disables Core Parking by default.
For the Brave
You may have noticed the game is mostly CPU bottlenecked. What can you do if your GPU usage is incredibly low and getting underutilized? Downsample! Render the game at a larger resolution, which makes textures sharper and jaggies disappear. Performance won't suffer until the GPU becomes the bottleneck. Find out how to do this in my other guide: http://www.reddit.com/r/elderscrollsonline/comments/26rkgb/play_eso_at_4k_on_any_monitor/
