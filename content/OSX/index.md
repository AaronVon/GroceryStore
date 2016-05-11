# Max OS X

![](/res/OSX_logo.jpeg)

This section stores some tips about Mac OS X.

---

##### 截图技巧
- 改变截图默认保存路径

<!-- lang:bash -->
	$ defaults write com.apple.screencapture location ~/Pictures/截图/
	
执行命令之后需要重启`SystemUIServer`。

-  改变默认格式

如改变为 `JPG` 格式，也可以把参数换为`GIF`、`TIF`、`PDF` 等。


<!-- lang:bash -->
	$ defaults write com.apple.screencapture type jpg
	
 同样需要重启`SystemUIServer`。
 
- 在窗口捕捉模式下，按住 `alt` 则可以捕捉不带阴影的截图
- 重启 `SystemUIServer` 
 
<!-- lang:bash -->
	$ killall SystemUIServer
	
---

##### Geek Dock

> From: [装点你的 Dock：外观篇丨一日一技 · Mac](http://sspai.com/33493)

- 增加空白占位符

![](/res/dock_placeholder.jpg)


在「应用区」:
	
<!-- lang:bash-->
	$ defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}'; Killall Dock
	
在「堆栈区」:

<!-- lang:bash -->
	$ defaults write com.apple.dock persistent-others -array-add '{tile-data={}; tile-type="spacer-tile";}'; Killall Dock
	
- 隐藏应用使用透明图标显示

使通过 `⌘H` 隐藏的应用图标半透明显示:

<!-- lang:bash -->
	$ defaults write com.apple.dock showhidden -bool true; Killall Dock
	
恢复默认设置:

<!-- lang:bash -->
	$ defaults delete com.apple.Dock showhidden; Killall Dock
	
- 设置最小化窗口效果为「吸入」效果
	- 神奇效果（Genie）
	- 缩放效果（Scale）
	- 吸入效果（Suck）

<!-- lang:bash -->
	$ defaults write com.apple.dock mineffect suck; Killall Dock
	
*恢复设置在系统偏好里*

- 而这一切只需要 [OnyX](http://www.titanium.free.fr) 则可以实现