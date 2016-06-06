# Mac 的加密手段

> Nothing is uncrackable, only your value makes the difference.

<br>

---

##### 固件密码 (Firmware Password)

> From: [为你的 Mac 添加「固件密码」保护 | 一日一技 · Mac](http://sspai.com/33355)

1. 关机
2. 按住 `⌘R` 开机，进入恢复模式
3. `实用工具` -> `固件密码实用工具` -> `开启固件密码`
4. 设置 `固件密码`
5. 重启电脑

> 开启固件密码（ Firmware Password ）来防止他人恶意从其它磁盘启动你的 Mac，重新安装系统 ，或通过恢复分区重置登陆密码或抹掉你的数据。

<br>

---

##### 创建 DMG 镜像

######方法1. 使用 Disk Utility 创建

######方法2. hdiutil 命令

- `创建 DMG 文件`

<!--lang:bash-->
	$ hdiutil create -fs HFS+J -srcfolder /path/inputfolder /path/output.dmg
	
-fs 指定创建格式。
	
- `创建加密的 DMG 文件`

<!--lang:bash-->
	$ hdiutil create -fs HFS+J -encryption AES-128 -srcfolder /path/inputfolder /path/output.dmg
	
-encryption 指定加密算法，默认为 `AES-128`，可以选择为 `AES-256`。

- `分割既有 DMG 文件`

<!--lang:bash-->
	$ hdiutil segment -segmentSize 1g -o <prefixname> /path/input.dmg
	
-segmentSize 指定切割大小

- `分割并加密 DMG`

<!--lang:bash-->
	$ hdiutil segment -segmentSize 1g -encryption AES-128 -o <prefixname> /path/input.dmg

**PS: 若需要分割之后的 DMG 文件也加密，则需要带入 `-encryption` 参数。与分割之前的文件加密与否无关。**

<br>

