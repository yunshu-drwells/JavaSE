<font size = 4 face = "黑体">



### 调试方式




### 添加警告忽略器

```
	public E get(int index) {
		return (E)elementData[index];
	}
```
> E是泛型类型，以上代码会警告
>
> warnings: unchecked cast from Object to E

方法：添加警告忽略语句（因为代码并没有逻辑错误而且是编译器太严格的原因）

添加如下语句：

    @SuppressWarnings("unchecked")

在警告位置前面

```
    @SuppressWarnings("unchecked")
	public E get(int index) {
		return (E)elementData[index];
	}
```
警告就被屏蔽了


### 快捷方式

|按键组合|功能|
|:---:|:---|
| <kbd>Alt</kbd>+<kbd>/</kbd>| 代码补全|
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>O</kbd>|自动引包|
| <kbd>Ctr</kbd> + <kbd>D</kbd>| 删除光标所在行|
| <kbd>Ctr</kbd> + <kbd>Backspace</kbd>| 删除光标前一个单词|
| <kbd>Ctr</kbd> + <kbd>T</kbd> |可以查看当前页面的类的继承关系|
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>Q</kbd>|重命名选中的变量, 修改范围是全文|
| <kbd>Ctr</kbd> + <kbd>鼠标左键</kbd>|点击任意类名或者变量名可以看源码|
| <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>箭头</kbd>|可复制光标所在行内容偏移向箭头方向一行|
| <kbd>Alt</kbd>+<kbd>箭头</kbd>|可移动光标所在行内容偏移向箭头方向一行|
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>S</kbd>|打开source窗口(可添加构造器、setters和getters等)|
| <kbd>Shift</kbd>+<kbd>Enter</kbd>|在光标所在行下方插入一行空白行，光标同时移动到新增空白行|
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd>，<kbd>J</kbd>|以JavaApplication运行|
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>Q</kbd>，<kbd>P</kbd>|打开Package Explorer窗口（悬浮状态时)|
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>Q</kbd>，<kbd>C</kbd>|打开Console窗口（悬浮状态的Console,不出来可以手动调出)|



</font>