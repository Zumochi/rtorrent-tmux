#rTorrent tmux init script for Debian

This is an initscript to run rTorrent on Debian

Original script by Super Jamie <jamie@superjamie.net>  
tmux conversion & new functions by Zumochi

####Requirements
* tmux and rtorrent
* A non-priviledged user to run rtorrent, this can either be a new user just to run torrents, or an existing user
* ***Absolute*** path to your session directory in .rtorrent.rc, e.g. `session = /home/user/.session`

####Installation
- Move or copy the script to /etc/init.d/rtorrent and make it executable
```
cp rtorrent /etc/init.d/rtorrent
chmod +x /etc/init.d/rtorrent
```
- *Optional:* Add an alias to your user environment for easier access
```
alias rtorrent='/etc/init.d/rtorrent'
alias rt='rtorrent'
```

####Usage
- *Note:* username is not needed if you're running the script for yourself
- Control the daemon with  
`rtorrent start (username)` to start  
`rtorrent stop (username)` to stop  
`rtorrent restart (username)` to restart
- Get information about the daemon with  
`rtorrent status (username)` to see the PID if it's running  
`rtorrent info (username)` to see more
- Connect to the tmux session with  
`rtorrent connect (username)` (press Ctrl+B, D to disconnect)

####Licensing
Released under GNU GPL v3 - http://www.gnu.org/licenses/

