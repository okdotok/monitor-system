![NetDash Logo](https://github.com/okdotok/monitor-system/blob/master/netdash1.png)

NetDash - v1.4.4 
======


Small web-based monitoring dashboard for windows in C and MVC
A small web-based monitoring dashboard for your Windows pc/server writen in C# and MVC + Chart.js.

The dashboard is built using only C# libraries available in the main C# distribution, trying to create a small list of dependencies without the need of installing many packages or libraries.

**Current dependencies**:

- Net Framework 4
- C# MVC 
- AttributeRouting
- SQLite

**Localization**:

- (1) "App_Data\Localization\en-EN.txt" copy this file and translate the language you want to use.
- (2) "App_Data\Setting.ini" LANGUAGE line in the file that you want to use the written language. Example: LANGUAGE=en-EN or LANGUAGE=tr-TR
- (3) Started to use in their own language

**Login info**

	user: admin
	pass: admin123

![NetDash](https://github.com/okdotok/monitor-system/blob/master/netdash-700x349.png)

**NetDash Settings**

The only settings currently available which you can modify are the refresh rates for the different data tables. There are 3 different refresh settings under *netdash/App_data/Setting.ini* and values are in miliseconds:


* TIME_JS_REFRESH = 30000       #30 seconds
* TIME_JS_REFRESH_LONG = 120000	#120 seconds
* TIME_JS_REFRESH_NET = 2000	#2 seconds

You can modify any of the values to whatever you would like the new refresh rate to be. Restart the webserver after each update to the Setting.ini file.

The tables and the refresh settings are as follows:

* Memory Usage - TIME_JS_REFRESH
* Load Average - TIME_JS_REFRESH
* CPU Usage - TIME_JS_REFRESH
* Traffic Usage - TIME_JS_REFRESH_NET
* Disk Reads/Writes - TIME_JS_REFRESH_NET
* Uptime - TIME_JS_REFRESH_LONG
* Disk Usage - TIME_JS_REFRESH_LONG
* Online Users - TIME_JS_REFRESH_LONG
* Processes - TIME_JS_REFRESH_LONG
* Netstat - TIME_JS_REFRESH_LONG

**Remote data retrieval**	

NetDash remote data retrieval
	
**App_Data\Setting.ini**

	; Remote or Local server name (Default local name machine name : .)
	; Sample remote server SERVERNAME=0.0.0.0
	SERVERNAME=ipaddress
	        
	; Remote server login info (Ony remote server)
	
	REMOTE_DOMAIN=domain.com
	REMOTE_USERNAME=Administrator
	REMOTE_PASSWORD=password

NetDash will allow you to retrieve data remotely if needed. This can be useful if you want to store any of the data in a database or another application.

- /info/uptime/				- Uptime
- /info/platform/hostname/		- Hostname
- /info/platform/osname/		- OS Name
- /info/platform/kernel/		- Kernel
- /info/getcpus/cpucount/		- Number of CPU cores
- /info/getcpus/cputype/		- Type/Name of CPU
- /info/memory/				- Memory Usage
- /info/cpuusage/			- CPU Usage in percentage(%), free and used
- /info/getdisk/			- Disk Usage
- /info/getusers/			- Online Users
- /info/getips/				- IP Addresses
- /info/gettraffic/			- Internet Traffic
- /info/getdiskio/			- Disk Reads/Writes
- /info/proc/				- Running Processes
- /info/loadaverage/			- Load Average
- /info/getnetstat/			- Netstat

To see the format of the JSON returned datasets or data you can access any of the URLs from your browser ex. http://domain.com/info/uptime/ 

**OS Support**

- NetDash was tested and runs under the following OSs:
- Windows 2000 NT
- Windows 2003 Server
- Windows 2008 Server
- Windows 2012 Server

**Credits**

Dashboard Template, Bootstrap, Font Awesome

**Roadmap**


