## Filesystem
- 不同的项目放在/src的不同的package就行（按照李乐的方法，加CATKIN_IGNORE）  
还是说用不同的workspace比较好？->那么不同workspace的devel/setup.bash都要加一遍加到.bashrc中？ 答案是肯定的
- 其实可以把package放在外面，需要的时候拿到workspace下进行编译。
- 接着上面的问题， 一个src下的新增一个package， 那么src下的cma kelist file需要做什么改动吗？还是说就不用管
- 一般Cmakelist要改哪些文件
- 对于有python的，是不是要改Cmake里的python相关的设置  

## 交叉编译
- 可不可以放一些python的文件在package，catkin_make之后能否识别rospack，（因为我原来有写过python的文档，直接python run出来就行，不用经过catkin_make，这区别是在于c需要生成可执行文件吗？）

## rqt_graph
-显示不全  
