What does an automatic Distance server need to do?
* Start on game launch (Name, large number of players, not private).
* Select a large playlist.
* Shuffle the playlist.
* Ready itself.
* Start the game.

From that point it needs to:
* Put itself into spectator mode.
* Determine if all players have finished.
  * If they have, go to the next level.
  * If they have not, wait for them to.
    * Put a max limit on the time so that the server doesn't spend too long on one level (e.g. Colorless). Max of maybe 10 mins?
    * Have a way for a majority of players (>50%) to vote to go to the next level.
* Upon starting the next level, go back into a loop starting with putting self into spectator mode.
* If the server reaches the end of the playlist, go back to the lobby, load the playlist again, shuffle it again, etc.

Potential commands:
* All users, majority-based:
  * !votenext
  * !voterestart
* Maintenance commands for operator/approved users:
  * !kill
  * !kick
  * !ban (a.k.a. autokick. maybe?)
  * !list

Include functionality to automatically display:
* Tips, Hints about server functionality (commands)
* Next level, next level author, etc.
* Welcome messages
* Server owner contact info, etc.
