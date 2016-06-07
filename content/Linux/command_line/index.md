# 常用命令

### du 

> display disk usage statistics

<!--lang:bash-->
	$ du -sh	# 显示当前目录的所有文件总和
	
<!--lang:bash-->
	$ du -d 1 -h ~/		#以深度为 1 显示 home 路径下所有目录大小

	
- 与 `sort` 配合排序输出

<!--lang:bash-->
	$ du -d 1 ~/ | sort -n # 由小到大输出 home 路径下一级目录大小
	
<!--lang:bash-->
	$ du -a ~/ | sort -rn # 由大到小输出 home 路径下所有文件大小