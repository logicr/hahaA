><font face ="幼圆"  caolor = "2F4F4F" size ="4"> 清楚我要学什么

<font face ="幼圆"  caolor = "2F4F4F" size ="4"> 之前有过打算学习一下Github，但是仅仅是创建好帐号之后就继续不下去了，一方面是没有编程方面的基础，头脑中没有`指令`的概念，还有就是没有一个合适的学习方法，只是在跟着教程敲git，但是不知道这些指令的用途，以及自己能用这些指令做什么。在最近的学习中，我逐渐形成了一个学习套路，就是在学习一个新知识之前，先了解一下这个知识体系的架构，形成一个知识脉络，然后清楚自己想在这方面学习哪方面的知识。
![思维导图](https://img-blog.csdn.net/20180323112732652?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
<font face ="幼圆"  caolor = "2F4F4F" size ="4">当然，这个思维导图是我学习完成之后才构建的，并非是我在学习之前就想好的，只是在学习中清楚自己需要哪方面的知识，有一个大体的脉络，然后不断的百度百度。

---

><font face ="幼圆"  caolor = "2F4F4F" size ="4">帐号注册

   [https://github.com/join](https://github.com/join)
![登录](https://img-blog.csdn.net/20180323113957934?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
><font face ="幼圆"  caolor = "2F4F4F" size ="4">建立仓库


![创建仓库](https://img-blog.csdn.net/20180323114914234?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)


><font face ="幼圆"  caolor = "2F4F4F" size ="4">安装就不说了，链接到远程仓库
		
<font face ="幼圆"  caolor = "2F4F4F" size ="4">安装完成之后，新建一个文件夹，鼠标右键，会出现一个 `Git Bash Here`点击就可以进行命令操作了

		 ssh-keygen -t rsa -C "email address"


<font face ="幼圆"  caolor = "2F4F4F" size ="4">一路回车就会生成一个`id_rsa.pub`
	
		cat ~/.ssh/id_rsa.pub
	
复制到Github
	
	点击头像 ->setting ->SSH and GPG keys ->new SSH key
![SSH](https://img-blog.csdn.net/20180323120530446?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
<font face ="幼圆"  caolor = "2F4F4F" size ="4">验证一下
	
	ssh -T git@github.com
![验证](https://img-blog.csdn.net/20180323121023243?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
<font face ="幼圆"  caolor = "2F4F4F" size ="4"> 设置username和email
	
	git config --global user.name "name"//Github 的名字
	git config --global user.email "Email address"//留的邮箱地址

><font face ="幼圆"  caolor = "2F4F4F" size ="4"> 设置、clone仓库

	
	    git remote add origin git@github.com/logicr/test
		git clone https://github.com/logicr/test
![clone](https://img-blog.csdn.net/20180323144254508?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

<font face ="幼圆"  caolor = "2F4F4F" size ="4">这样本地就clone了Github上刚刚新建的仓库

><font face ="幼圆"  caolor = "2F4F4F" size ="4">提交修改
	
	vim show.md//创建一个md文件叫Show，也可以在本地仓库用记事本写一个
	"我叫Jan，正在学习Github"
	
![show](https://img-blog.csdn.net/20180323123322373?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
<font face ="幼圆"  caolor = "2F4F4F" size ="4">上传
	
	git add "show.md"
	git commit -m "this is a show file"
	git push origin master
![code](https://img-blog.csdn.net/20180323123145741?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
<font face ="幼圆"  caolor = "2F4F4F" size ="4">先看看我的仓库没有提交之前的样子
![kankan](https://img-blog.csdn.net/20180323123959533?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
<font face ="幼圆"  caolor = "2F4F4F" size ="4">提交之后，与之前相比，里面多了一个show.md，打开之后，就可以看到我的之前写的自我介绍。
![提交之后](https://img-blog.csdn.net/20180323124148133?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

<font face ="华文行楷"  caolor = "2F4F4F" size ="4">到此，终于算是小有所成能够将本地修改提交到远程仓库里，但是，这只是Github的基本功能。但是在使用中有一些其他需求，比如，我把刚刚刚的show.md删除
><font face ="幼圆"  caolor = "2F4F4F" size ="4">删除文件

	
	git rm -r --cached "show.md"
	git commit -m "delete show"
	git push origin master
![delete](https://img-blog.csdn.net/20180323133622145?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
<font face ="幼圆"  caolor = "2F4F4F" size ="4">再来看看的仓库，看看的show.md，已经被删掉。
![gone](https://img-blog.csdn.net/20180323133752782?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
<font face ="幼圆"  caolor = "2F4F4F" size ="4">不过，Github怎么可能让你轻易删掉文件
><font face ="幼圆"  caolor = "2F4F4F" size ="4">版本回退

<font face ="幼圆"  caolor = "2F4F4F" size ="4">如果是删除文件
查看日志
	
	git log 
![recovery](https://img-blog.csdn.net/20180323135525355?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
<font face ="幼圆"  caolor = "2F4F4F" size ="4">这里的语句` I delete show`，表示这是我刚刚的删除操所，这时候才显示出 `git commit -m "txt"`里面文本的重要性，要不然过几天之后，一堆没有说明的日志文件根本无从查找。复制commit 后面的ID
	
	git reset --hard ID//如果仅仅上前一次的操作可以不用ID,git reset --hard HEAD^

<font face ="幼圆"  caolor = "2F4F4F" size ="4">那么现在再将文件提交即可。
如果是会退到之前版本，步骤都一样，先修改一次，在hide.md后面添加一句`“我现在修改一次，提交到Github”`
![change](https://img-blog.csdn.net/20180323141655691?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

	git reset --hard ID//如果仅仅上前一次的操作可以不用ID,git reset --hard HEAD^
	
<font face ="幼圆"  caolor = "2F4F4F" size ="4">再push一次

	git push origin master
![error](https://img-blog.csdn.net/20180323142525620?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
<font face ="幼圆"  caolor = "2F4F4F" size ="4">不过会报错，因为文件的add和commit还是之前的，但是不用再次add和commit那么麻烦
	
	git push origin master --force
![success](https://img-blog.csdn.net/20180323142932252?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0xvZ2ljcg==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)
<font face ="幼圆"  caolor = "2F4F4F" size ="4">内容就已经成功回退到上一次的状态。
终于把这些基本操作有所了解，之后再学习一下分支，标签。
在这次学习中参考了资料：[菜鸟教程-github简明教程](http://www.runoob.com/w3cnote/git-guide.html)、[廖雪峰的官方网站github教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013744142037508cf42e51debf49668810645e02887691000)，[以及大量网友热心回复等，不在一一列举](https://blog.csdn.net/Logicr)，这些资料对我的学习带来了巨大帮助，在此感谢。