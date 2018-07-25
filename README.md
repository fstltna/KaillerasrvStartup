# Kaillera Server Startup Scripts (2.0.0)
Startup scripts for the Kaillera game server - uses the "screen" command to manage session. This also restarts the Kaillera server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/KaillerasrvStartup)

---
These start up the Kaillera server at boot time with a "screen" process.

1. Copy **kaillera** into **/etc/init.d** - make sure it is executable
2. Copy **startkaillera** into **/root/kaillerasrv-0.86** - make sure it is executable
4. Run "**systemctl enable kaillera**" (only needed once, will stick)
5. Run "**systemctl start kaillera**" - starts Kaillera without restarting the server

When you want to view the Kaillera console, just enter "**screen -r**" in your shell.

To disconnect from the Kaillera console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/kaillerasrv-0.86/nostart**". To reenable it type "**rm /root/kaillerasrv-0.86/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
