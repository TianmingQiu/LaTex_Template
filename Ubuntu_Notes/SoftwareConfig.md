## Matlab
1.在/usr/bin中新建文件,"matlab"

`$ sudo vim matlab`

这里的文件名matlab就是以后在命令行打开matlab程序的命令.

2.在文件中写入
```
#!/bin/bash'

$matlab_Path
```

这里"$matlab_Path"换成可执行文件MATLAB的路径就行了,例如我的是:/usr/local/MATLAB/R2017b/bin/matlab.保存,退出.

3.回到/usr/bin中更改新建文件matlab的权限

`$ sudo chmod 777 matlab`

4.使用命令行到任意路径下输入:matlab.


## 在Annaconda Python 2.7 基础上继续添加 Python 3.6的[方法](https://conda.io/docs/user-guide/tasks/manage-python.html)

## TensorFlow 
- 安装[pip](https://pip.pypa.io/en/latest/installing/#id7)
- 安装[TensorFlow](https://zhuanlan.zhihu.com/p/24055668)： `pip install --upgrade --ignore-installed tensorflow` (CPU版)

## 优雅使用sublime
- `sudo ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl`  
然后直接在命令行中输入subl

## Install google pinyin input method [link](https://blog.csdn.net/zhuyucheng123/article/details/53184490)  
