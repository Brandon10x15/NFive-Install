# NFive-Install
A quick guide to walk you through the already quick and easy installation process.

NFive Quick Install Instructions

	Prerequisites:
		MySQL Server


	1. (Optional) Move 'nfpm.exe' and 'nuget.exe' to your 'Local Disk (C:)\Windows' folder in order to use it in other directories.


	2. Open Command Prompt and do the following to start the NFive setup and install 2 plugins.

"

	C:\Users\Home>cd C:\GTA\nFive

	C:\GTA\nFive>nfpm setup

This utility will walk you through setting up a new FiveM server with NFive installed.

The server will be installed at C:\GTA\nFive\server

Press Ctrl+C at any time to quit.

	Install FiveM server?: (yes)

FiveM server configuration...

	server name: (NFive) YOUR_SERVER_NAME
	server max players: (32)
	server locale: (en-US)
	enable OneSync: (yes)
	server tags (separate with space): (NFive) default roleplay nfive
	server license key (https://keymaster.fivem.net/): YOUR_FIVEM_SERVER_KEY
	Steam API license key (https://steamcommunity.com/dev/apikey): (<disabled>) YOUR_STEAM_API_KEY
	RCON password: (<disabled>) **********
	
Finding available FiveM Windows server versions...
567 versions available, latest v2943, recommended v2430, optional v2443

	FiveM server version: (latest)

Reading FiveM Windows server v2943 from cache...
Installing FiveM Windows server...

	Install NFive?: (yes)

NFive database configuration...

	database host: (localhost)
	database port: (3306)
	database user: (root)
	database password: (<blank>) YOUR_DATABASE_PASSWORD
	database name: (fivem)

Finding latest NFive version...
Reading NFive v0.6.0.219 from cache...
Installing NFive...
	
Installation is complete, you can now start the server with `nfpm start`!

	C:\GTA\nFive>cd server

	C:\GTA\nFive\server>nfpm install NFive/plugin-loadingscreen

https://hub.nfive.io/api/project/NFive/plugin-loadingscreen.json
+ NFive/plugin-loadingscreen@^1.3.0

	C:\GTA\nFive\server>nfpm install NFive/plugin-start

https://hub.nfive.io/api/project/NFive/plugin-start.json
+ NFive/plugin-start@^1.5.1
https://hub.nfive.io/api/project/NFive/plugin-loadingscreen.json
"

	3. Run 'nfpm start' to test start the server.

"

	C:\GTA\nFive\server>nfpm start

Starting server...
Press Ctrl+C to exit
Creating script environments for _cfx_internal
Found new resource nfive in C:/GTA\nFive\Install\server/resources//nfive
Found new resource monitor in C:\GTA\nFive\Install\server\citizen/system_resources//monitor
Found new resource webadmin in C:\GTA\nFive\Install\server\citizen/system_resources//webadmin
←[93mCouldn't find resource sessionmanager.←[0m
Creating script environments for monitor
Started resource monitor
Creating script environments for nfive
2020-09-09T23:07:05 [Info] NFive 0.6.0.219-alpha
2020-09-09T23:07:08 [Info] Loading NFive/plugin-loadingscreen@1.3.0
2020-09-09T23:07:08 [Info] Loading NFive/plugin-start@1.5.1
2020-09-09T23:07:08 [Debug] 2 plugin(s) loaded, 3 controller(s) created
2020-09-09T23:07:08 [Info] Server ready
Instantiated instance of script NFive.Server.Program.
2020-09-09T23:07:08 [Trace] [FiveM] Triggered: onResourceStart
Started resource nfive
[93mWarning: `onesync_enabled` is deprecated. Please use `onesync legacy` instead.
[0mAuthenticating server license key...
cfx> Server license key authentication succeeded. Welcome!
[93mAuthenticating with Nucleus...[0m
[91m        fff
[91m  cccc ff   xx  xx     rr rr    eee
[91mcc     ffff   xx       rrr  r ee   e
[91mcc     ff     xx   ... rr     eeeee
[91m ccccc ff   xx  xx ... rr      eeeee
                                     [0m
[32mAuthenticated with cfx.re Nucleus: [0mhttps://brandon10x15-8lkklm.users.cfx.re/
Sending heartbeat to https://servers-ingress-live.fivem.net/ingress

	C:\GTA\nFive\server>
"

	4. Press Ctrl+C to stop the server and keep the command prompt open.

	5. Navigate to your server folder, 'C:\GTA\nFive', and open 'server.cfg' in a text editor.

	6. Port forward the default server port, '30120', or change the following and port forward your own port. 
	Leave the [::] alone and only change the port to your own.
	"
	endpoint_add_tcp "[::]:30120"
	endpoint_add_udp "[::]:30120"
	"

	7. Open the command prompt we were using and run 'nfpm start' in your server folder, 'C:\GTA\nFive\server'.

	8. Open up FiveM and navigate to the settings icon at the top right.
	Check 'enable the "localhost" menu item'.
	Enter your port in the 'Custom port' box.
	Click the FiveM logo at the top left.
	Click the 'LOCALHOST' button to connect to your server.
	(Alternative)
	Open up FiveM and click the 'PLAY' button.
	Search your server name or ip address.
	Click your server to view more info and click the star icon to favorite it.
	Connect to your server.
