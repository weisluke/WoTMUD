# WoTMUD
WoTMUD triggers/aliases/scripts/timers/keys/buttons/maps

1. Download and save "wotpack_installer.mpackage" somewhere easy to find on your computer.
2. Open Mudlet, open Package Manager (from the top toolbar of icons), and click install.
3. Navigate to the location you saved the .mpackage file, select it, and click open. It should now show up in the list of packages. Cick ok.
4. You should see an automatic help message from the package installation on your screen.
   1. If not, try typing "wotpack install help" into the command line and hit enter.
   2. If no help message appears, something may have gone wrong.

Assuming everything worked properly, what you have just installed is a script that will handle downloading and installing other triggers/aliases/scripts/timers/keys/buttons/maps from this repository via commands sent through Mudlet.

5. To get a map, you will want to uninstall the generic mapper in Package Manager (if it is in there), then reopen Mudlet.
6. Type "wotpack install mapper" into the command line and hit enter.
   1. If things are successful, you should receive some messages along the lines of "(wotpack_installer): New mapper_scripts successfully installed."
7. When that completes, type "map update". You should again recieve some messages about the map file downloading and installing. This may take a moment depending on your internet speed.
   1. Look at your room, and see if the map centers on your position. Then try moving around.
   2. You may see debugging messages next to room names, room exits, and direction inputs. You can type "map debug" to turn them off.

7. To get a communications window that stores says/chats/nars/etc, type "wotpack install communications". 
8. I did NOT write this comms window, so will only be of minimal help if it misbehaves.
9. You may need to restart mudlet again for the comms window to look nicer/take effect.

10. You can type "wotpack view files" to get a list of all possible files available for download. This list is NOT displayed very neatly, hopefully I can change that in the future. You can use commands from the help message to install particular pieces, or everything. Most names should be self explanatory.


11. Please check the forums (http://www.wotmod.org/index.php) or the game discord (http://www.wotmod.org/viewtopic.php?f=74&t=7300) for more assistance if need be. I should be able to be reached by tagging @weisluke in the discord (preferably in the "mudclient_helpdesk" channel)
