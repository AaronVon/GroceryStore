# Lanuchpad

##### 改变 Launchpad 中图标大小

- **第一步:** 设置 Launchpad 的列数

<!--lang:bash-->
	$ defaults write com.apple.dock springboard-columns -int 8

- **第二步** 设置 Launchpad 的行数

<!--lang:bash-->
	$ defaults write com.apple.dock springboard-rows -int 7
	
- **第三步** 重置 Launchpad

<!--lang:bash-->
	$ defaults write com.apple.dock ResetLaunchPad -bool TRUE
	
- **第四步** 重置 Dock

<!--lang:bash-->
	$ killall Dock