# This is mainly a guide for a selfhosted LOCAL server for online access more has to be done will update maybe later

1. Create a Folder for SteamCMD (End size is around 32GB)
  - I chose E:/Games/steamcmd
2. Download SteamCMD via https://steamcdn-a.akamaihd.net/client/installer/steamcmd.zip
3. Extract .zip file to newly created folder
4. Enable File name extensions (In Win10 this is a checkbox in the View Tab of the File explorer)
5. Rightclick in the steamcmd folder  New -> Text file 
6. Insert "steamcmd.exe +force_install_dir ./cs_go/ +login anonymous +app_update 740 +quit" without quotes and save
7. Exit Notepad and change the extensions from .txt to .bat
8. Open the new file (a black console window should appear and start downloading everything for you, that might take a while )
 - In the meantime visit https://github.com/splewis/csgo-practice-mode and click on the latest Release on the right side (1.3.4 currently)
  - Download the practicmode_1.3.4.zip or whatever version it is
  - Visit https://www.sourcemod.net/downloads.php?branch=stable and click the Windows Icon 
  - Visit http://www.metamodsource.net/downloads.php?branch=stable and click the Windows Icon
9. Open CSGO for now (and find out how to open the console if you don't already know how)
10. Open the steamcmd/cs_go/csgo folder 
11. Extract the Metamod zip to the steamcmd/cs_go folder
12. Just for the testing go back to steamcmd/cs_go 
13. Create a new bat file with the following command "start srcds.exe -game csgo -tickrate 128 -console -usercon +game_type 0 +game_mode 1 +mapgroup mg_active +map de_inferno -maxplayers_override 32 +port 27016 " you can change the tickrate to 64 or just create two bat files with different tickrates
14. Find out your local ip (for example open Command Prompt and type "ipconfig" remember your ipv4 address
15. Open csgo (dont click the .bat before)
16. Double click the newly created start.bat a black window should open up again
17. In the csgo game type "connect youripv4:27016" youripv4 = the just gotten ipv4 address it should connect to the server
18. In the console type "meta version" just to test if everything installed correctly
19. Also type in status and copy and save your steamid somewhere (should be next to your name and look like this STEAM_1:0:1300xxx 
20. Type "quit" sgoserver console
21. Go back to steamcmd/cs_go/csgo
22. Extract the sourcemod.zip inside this folder 
23. (If you want you can restart the server via the bat file , reconnect and type "meta info" to check if sourcemod installed correctly should output
```
] meta list
  [01] SourceMod (1.11.0.6934) by AlliedModders LLC
  [02] CS Tools (1.11.0.6934) by AlliedModders LLC
  [03] SDK Tools (1.11.0.6934) by AlliedModders LLC
```
  - quit inside server console again
24.
25. Go to steamcmd\cs_go\csgo\addons\sourcemod\configs 
26. Open admins_simple.ini and add this "STEAM_1:0:1300xxx" "99:z"	just replace STEAM_1:0:1300xxx with your steamid (this time actually use the quotation mark
27. If you want you can start the server again type in "sm_admin" to test if you are a admin a admin menu should pop up
28. Extra the practicemode.zip to steamcmd\cs_go\csgo and start server
29. Type .prac inside the game (not the console) for other commands look at the list on https://github.com/splewis/csgo-practice-mode



















