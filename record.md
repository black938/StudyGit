# 记录一下Git的各种命令

- git init
	初始化仓库
	
- git add file_name
	添加文件进去
	
- git commit -m ""
	添加注释
	
- git log

  查看记录

- git reset --hard HEAD^

  回退到上一个版本（HEAD^ HEAD^^ HEAD-100）

- git log

  显示提交历史 commit id【以便确定要回退到哪个版本】

- git reflog

  （reference log）显示命令历史 【以便确定要回到未来的哪个版本】

```
关于reset和revert
如果已经有A -> B -> C，想回到B：

方法一：reset到B，丢失C：

A -> B

方法二：再提交一个revert反向修改，变成B：

A -> B -> C -> B

C还在，但是两个B是重复的

看你的需求，也许C就是瞎提交错了（比如把密码提交上去了），必须reset

如果C就是修改，现在又要改回来，将来可能再改成C，那你就revert
```

- 