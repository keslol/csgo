1. Create a Folder for SteamCMD (End size is around 32GB)
  - I chose E:/Games/steamcmd
2. Download SteamCMD via https://steamcdn-a.akamaihd.net/client/installer/steamcmd.zip
3. Extract .zip file to newly created folder
4. Open the steamcmd.exe a console window should open and download data (don't close this window for now)

For this section you can just rightclick the console window to paste instead of retyping commands

6. A prompt (Steam>) should be shown type "force_install_dir ./cs_go/" without the quotes
7. Now type in "login anonymous"
8. Now "app_update 740 validate" (This will take a while depending on internet speed
9. To update the application you can just use the same commands or write a .bat file (In the Update Script section)

























### Update Script
1. Enable File name extensions (In Win10 this is a checkbox in the View Tab of the File explorer)
2. Rightclick in the steamcmd folder  New -> Text file 
3. Insert "steamcmd.exe +force_install_dir ../cs_go +login anonymous +app_update 740 +quit" and save
4. Exit Notepad and change the extensions from .txt to .bat
