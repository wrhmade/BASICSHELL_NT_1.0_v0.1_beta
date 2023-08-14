BASICSHELL NT 简介
 _______     ___    ______   _   ______
|   __  |   / _ \  /  ____| | | /  ____|  _____        _____                 ___    _   _____
|  |__| |  | |_| | | (___   | | | |      /       |    /     \ |     |       |   \  | | |_   _|
|   ___  \ |  _  |  \__  \  | | | |      \_____  |__  |_____/ |     |       | |\ \ | |   | |
|  |___| | | | | |  ___)  | | | | |____        \ |  | |       |     |       | | \ \| |   | |
|________| |_| |_| |_____/  |_| \______| ______/ |  | \______ |____ |____   |_|  \___|   |_|
BASICSHELL NT全称"BASICHSELL New Technology"，是以EasyX Core为内核的BASICSHELL
BASICSHELL与BASICSHELL NT的区别


类别\系统	BASICSHELL		BASICSHELL NT
=====================================================
内核		BASICKERNEL		EasyX Core
编写语言		Python			C++
用户数量		多用户(3.3+)		单用户
默认用户		System			@manager #64
适用系统		Windows/Linux/MacOS	Windows
=====================================================
虚拟系统		N			Y
文件管理		Y(3.2+)			Y
文件系统		N			Y
=====================================================
面向领域		家用			商业
=====================================================


因为BASICSHELL NT使用C++编写，所以无需安装Python解释器
而BASICSHELL使用Python编写，所以需要安装Python解释器

BASICSHELL NT新功能:
 - 虚拟系统
 - 文件系统


文件系统原理:


索引              文件系统末端
  |              |
  |              |
[0][1][2][3][4][5][6][7][8][9][10]
 \___可访问区域__/  \_不可访问区域_/


索引
  ├──文件名(字符串型)
 ├──文件内容(字符串型)
 └──是否使用(布尔值型)



索引:存储一个文件的区域
可访问区域:文件系统中可以访问的区域
不可访问区域:文件系统中不能访问的区域
文件系统末端:可访问区域的最后一个索引
文件名:文件的名称
文件内容:文件的内容
是否使用:文件索引是否使用,未使用则代表空索引