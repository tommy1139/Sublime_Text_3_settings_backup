# Sublime_Text_3_settings_backup
For Sublime Text 3 user folder backup

將 dropbox 的 user backup 資料夾建立一個軟連結取代現存的 sublime user 資料夾 

出處:
https://adamdehaven.com/blog/how-to-sync-sublime-text-packages-and-settings-across-multiple-computers-with-dropbox/

1. Close down Sublime Text
2. Open PowerShell by right-clicking and selecting “Run as administrator” and then enter the following commands

# Navigate to the Sublime Text 3 Package directory
cd "$env:appdata\Sublime Text 3\Packages"

# Create a symlink within the Sublime Text 3 Package directory pointing to the User folder within Dropbox/Sync/Sublime Text/ directory.
cmd /c mklink /D User "$env:userprofile\Dropbox\Sublime\Sublime_Text3_settings"