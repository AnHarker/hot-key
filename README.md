快捷键

切换终端

	Ctrl+Alt+F[1-6] 
		CentOS 6 	Ctrl+Alt+F[1-6]为命令行界面   	Ctrl+Alt+F7为图形界面
		CentOS 7 在哪个终端启动，即为哪个虚拟终端

screen命令


	剥离当前screen会话
		Ctrl+a,d

tab键

	给出唯一的命令、文件或路径，将直接补全
	否则双击TAB键将给出列表

命令行历史

	↑键↓键		为浏览从前输入的命令
	
	!!并回车 	为执行最近的一条命令
	
	!-N并回车 	为倒数第N条命令
	
	!：0并回车	为执行前一条命令无参数(0为不可改)
	
	!N并回车  	为执行history命令输出中对应正序的命令 (N为数字)
	
	!-N并回车	为执行history命令输出中对应倒序的命令 (N为数字)
	
	!string 	重复前一个以"string"开头的命令(可以简写)
	
	!?string	重复前一个包含string的命令
	
	!string:p	打印该命令
	
	!$:p		打印!$(上个命令的最后一个参数)的内容
	
	!*:p		打印!*(上一条命令的所有参数)的内容
	
	Ctrl+r		在命令历史中搜索命令
	
	Ctrl+g		从命令历史搜索中退出
	

	调用前一个命令中最后一个参数
		!$
		ESC,.(松开)
		Alt+.

	历史参数的调用
		COMMAND !^			使用上个命令的第一个参数做当前命令的参数
		
		COMMAND !$			使用上个命令的最后一个参数做当前命令的参数
		
		COMMAND !*			使用上个命令的全部参数做当前命令的参数
		
		COMMAND !:N  		使用上个命令第N个参数做当前命令的参数
		
		COMMAND !N:^		调用第N条命令的第一个参数
		
		COMMAND !N:$		调用第N条命令的最后一个参数
		
		COMMAND !N:M		调用第N条命令的第M个参数		
		
		COMMAND !N:*		调用第N条命令的所有参数
		
		command !string:^ 从命令历史中搜索以string 开头的命令，并获取它的第一个参数
		
		command !string:$ 从命令历史中搜索以string 开头的命令,并获取它的最后一个参数
		
		command !string:n 从命令历史中搜索以string 开头的命令，并获取它的第n个参数
		
		command !string:* 从命令历史中搜索以string 开头的命令，并获取它的所有参数		

bash(Alt容易和其他软件冲突)


	Ctrl+l		清屏，相当于clear命令	
	Ctrl+o  	执行已输入的命令并再次显示命令
	Ctrl+s 		阻止屏幕输出,相当于锁屏但不阻止输入	
	Ctrl+q 		允许屏幕输出
	Ctrl+c 		终止命令
	Ctrl+z 		挂起命令
	Ctrl+a 		光标移至命令行首，等于Home
	Ctrl+e 		光标移至命令行尾，等于End
	Ctrl+f 		光标在命令中右移动一个字符
	Ctrl+b 		光标在命令中左移动一个字符
	Ctrl+u 		从光标出删除至命令行首
	Ctrl+k 		从光标出删除至命令行首
	Ctrl+w 		从光标处向左删除至单词词首	
	Alt+d 		从光标处向右删除至单词词尾
	Ctrl+d	 	删除光标处的单个字符(若没有输入命令则退出当前SHELL)
	Ctrl+h 		删除光标前的单个字符
	Ctrl+xx 	光标在当前位置与命令行首间移动
	ALt+f 		光标向右移动一个单词且在词尾
	ALt+b 		光标向左移动一个单词且在词首
	Alt+r 		删除所在行(整行)
	Ctrl+y		将删除的字符粘贴至光标后
	Alt+c		从光标处开始向右更改为首字母大写的单词
	Alt+u		从光标处开始，将右边一个单词更改为大写
	Alt+l		从光标处开始，将右边一个单词更改为小写
	Ctrl+t		交换光标处和之前的字符位置
	Alt+t		交换光标处和之前的单词位置
	Alt+N		提示输入指定字符后，重复显示该字符N次

man

	向文件尾部翻屏		space, ^v, ^f, ^F
	向文件首部翻屏 		b, ^b
	向文件尾部翻半屏 		d,^d
	向文件首部翻半屏 		u,^u
	向文件尾部翻一行 		RETUEN(删除键), ^N, e, ^E, j, ^j
	向文件首部翻一行		y, ^Y, ^P, k, ^K
	退出					q
	跳转至NUM行 			NUM
	回到文件首部			1G
	翻至文件尾部 			G

		/KEYWORD  		以KEYWORD为关键字从当前位置向文件尾部搜索(不区分大小写)
		?KEYWORD    	以KEYWORD为关键字从当前位置向文件首部搜索(不区分大小写)
			n			跟搜索命令同方向，下一个
			N 			跟搜索命令相反方向，上一个

info

	方向键, PgUp, PgDn	导航
	TAB键 				移至下个链接
	d 					显示主题目录
	Home  				显示主题首部
	Enter 				进入所选链接
	n 					上一层链接
	p 					前一层链接
	u 					上一层链接
	l 					最后一个链接
	s 文字 				文本搜索
	q  					退出info
