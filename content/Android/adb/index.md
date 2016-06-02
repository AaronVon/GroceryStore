# ADB

#### Android Debug Bridge

<!--lang:bash-->
	$ adb connect <device-ip>:<port>
	
	$ adb install -r <name.apk>
	
	$ adb uninstall <name.apk>
	
	$ adb pull <remote> <local>
	
	> Demo: adb pull /sdcard/file.a ~/
	
	$ adb push <local> <remote>