## Filesystem
- 不同的项目放在/src的不同的package就行？（按照李乐的方法，加IGNORE）  
还是说用不同的workspace比较好？->那么不同workspace的devel/setup.bash都要加一遍加到.bashrc中？
- 接着上面的问题， 一个src下的新增一个package， 那么src下的cmakelist file需要做什么改动吗？还是说就不用管
- 一般Cmakelist要改哪些文件

## 交叉编译
- 可不可以放一些python的文件在package，catkin_make之后能否识别rospack，（因为我原来有写过python的文档，直接python run出来就行，不用经过catkin_make，这区别是在于c需要生成可执行文件吗？）
