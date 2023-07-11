命令行模式
输入模式
可视化模式
底行模式

a i o  进入输入模式
v       进入可视化模式    v也可出  
esc   进入命令模式
：     进入底行模式     操作完自动返回命令模式

rm  .1.php.swp


命令行下：
	yy      单行复制
	nyy    n行复制
	p        粘贴
	dd     单行剪切
	ndd   n行剪切
	u       撤销  <
	‘ctrl’+r  恢复 >
	gg    光标移动到首航
	G     光标移动到末行
	nG    光标移动到n行
	0      光标运动到行首
	$      行尾
	gg=G  整理代码格式
	/内容  查找    实际上是进入底行模式 ‘ / ’
		在搜索结果中切换上/下一个结果：N/n （大写N代表上一个结果，小写n代表next）
输入模式：
	i o a
	Backspace   向左删除
	Delete           向右删除
底行模式：
	w 保存
	q 退出
	wq 保存退出
	！强制
	q！强制退出
	w！强制保存
	n,n1y 指定行复制
	s/被替换/替换  替换光标所在行的第一个
	s/被替换/替换/g  替换光标所在行的所有
	1,$ s/被替换/替换/g  替换全文所在行的所有
	% s/被替换/替换/g  替换全文所在行的所有
	set nu  显示行号
	set nonu  取消显示行号
可视化模式：
	v  
	'Ctrl'+v  列模式
	y           复制
	p            粘贴