# 截图技巧
---

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