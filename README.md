## 1.SVN资源同步工具使用说明
> SVN同步工具下载:[https://tortoisesvn.net/downloads.html](https://tortoisesvn.net/downloads.html "https://tortoisesvn.net/downloads.html")

> SVN地址：[http://10.0.204.253/!/#AllResources](http://10.0.204.253/!/#)，使用Google浏览器或其他兼容性高的浏览器打开

当前SVN目录结构如下

- AllResources:新SVN工作目录,里面按不同的游戏项目进行分类,在此进行**视频制作**
- project:**资源库**,需要将其下载到UE4工程的**Content**文件夹下才可以使用
- work: **停用**
![](https://i.imgur.com/6mOrxJc.png)

使用SVN同步工具获取SVN资源
![](https://i.imgur.com/SISHBL2.png)

1. 复制Repository URL地址
2. 安装了SVN同步工具之后,在电脑的某个盘中同步刚刚的SVN地址,右键会出现以下界面,选中红框标记的选项
3. ![](https://i.imgur.com/E1uXn2u.png)
4. ![](https://i.imgur.com/WQG86gY.png)
5. 以上仅仅是演示之用,具体同步哪些资源以及使用方式,需根据自己工作内容决定


## 2.UE4目录结构说明
> 了解当前 **SVN** 工作原理之前,还需要掌握 **UE4** 的工作原理

- 这一部分内容极其重要,涉及到当前SVN结构的工作原理,以及UE4中的操作方式
- 创建UE4工程后会包括以下目录,所有的资源都要放在 **Content** 文件夹内
 ![](https://i.imgur.com/dMIFTo8.png)
- 现在回看最开始的:SVN目录结构的project和work文件夹,这两个文件夹必须在UE4工程的Content下才能使用,所以当你第一次使用SVN同步资源的时候,需要在本地自行创建一个UE4工程,然后将project和work文件夹在你新建的工程里面的Content文件夹中Checkout下来才可以使用,正确操作后会得到如下的目录结构,这里仅仅是演示操作方式,并不是要求完全这样操作
- ![](https://i.imgur.com/SdPrWwA.png)
- UE4对文件路径的识别极其严格,如:Content/A/B/**mat.material**,那么将mat转移到其他UE4工程的时候,也必须是在Content/A/B/这样目录层次下才可以准确识别,否则就会出现错误

## 3.AllResources目录结构说明
![](https://i.imgur.com/CigpnEA.png)

- AllResources
 - Mergical
 		- EffectProjects
 		- ModelProjects
 		- SceneProjects
 			- 常运康
 				- 20190130小萝莉指点江山1(UE4工程) 
 				- 20190131小萝莉指点江山2(UE4工程) 
 				- 20190132小萝莉指点江山3(UE4工程) 
 				- 20190133小萝莉指点江山4(UE4工程) 
 			- 杜玉茹 
 			 	- 20190130剧情展示1(UE4工程) 
 				- 20190131剧情展示2(UE4工程) 
 				- 20190132剧情展示3(UE4工程) 
 				- 20190133剧情展示4(UE4工程) 
 - GolfRival
   		- EffectProjects
 		- ModelProjects
 		- SceneProjects
 			- 刘畅 
 - Townest
   		- EffectProjects
 		- ModelProjects
 		- SceneProjects
 - 其他项目


----------


1. 以上是AllResources目录的结构
2. 每个视频制作人员会有独立的同名文件夹,在自己同名的文件夹下创建UE4工程,完成视频制作,需要地编人员提供场景的,由地编同学完成UE4工程的创建,其他的则由自己创建UE4工程 
3. 例如常运康,参与制作Mergical的项目,可以选择拉取SVN上的Mergical目录,拉取AllResources也没关系,因为每个人视频制作人员只对自己所负责的文件夹有读写权限,对其他文件夹仅有只读权限,所以不用担心误操作影响别人的东西
4. 新增的视频人员,以及其他等支持人员需要开通权限的,钉钉@龙闯 开通权限

## 4.SVN资源上传操作说明
1. 视频制确定可以开始的时候,如果视频需要地编提供场景制作,则UE4工程由地编创建,否则由视频制作人员创建UE4工程,其他同事需要协同工作,所以一开始就需要创建一个空的UE4工程,后续资源陆续上传即可
2. 创建好工程之后,上传UE4工程到SVN,不需要上传全部文件夹!具体需要上传的文件夹如下,只需要上传以下三个文件夹内的所有内容,其他的不要传:
3. ![](https://i.imgur.com/iyrVhqn.png)
4. 将不需要上传的文件夹,添加到忽略列表,具体操作如下
5. ![](https://i.imgur.com/2JJs5i2.png)

## 5.动作资源如果要导入给视频人员该如何操作?
1. 为了目录结构看起来更清晰,拉取AllResources的SVN目录到本地磁盘
2. 如当前某个动作师同学,需要将几个动作传入到指定视频同学的工程中,怎么做,操作如下
3. 找到视频同学的工程文件,例如需要将动作导入谈展豪的养成展示的视频工程中,双击启动**养成展示.uproject**将会启动UE4工程
4. ![](https://i.imgur.com/2Pl8mQq.png)
5. 打开工程之后会出现以下界面结构,UE4中所有的资源以及可以操作的文件,其实就是**Content文件夹**内的资源
6. ![](https://i.imgur.com/1GWOzt3.png)
7. ![](https://i.imgur.com/Hn9wigQ.png)
8. 所以动作师同学为了避免和其他人冲突,可以在UE4里面创建一个属于自己的文件夹,与动作相关的文件都上传到这个文件夹内,方便各位同学协同工作
9. 假设动作师同学创建了文件夹Animation,那么只需要在SVN中上传该文件夹即可,无需操作所有文件夹的上传工作
10. ![](https://i.imgur.com/v64WkLo.png)
11. 那么你新建的文件夹处于一个不在待提交的列表中,只需要右键Add到待提交列表即可
12. ![](https://i.imgur.com/nnOF2Tr.png)
13. Add成功之后会出现以下的蓝色加号,如果没有就刷新以下
14. ![](https://i.imgur.com/beQfSqk.png)
15. 此时就可以进行提交操作，如果没有将其Add，右键Animation文件夹是没有Commit选项的
16. ![](https://i.imgur.com/TrMZjCj.png)
17. 至此，关于动作师同学的操作就这些


---
## 6.文件夹如何断开与SVN的链接？
1. 在查看中，将隐藏的项目一项勾选打开，删除.svn文件夹之后，整个文件夹就变成普通文件夹，不再与SVN同步，SVN的一些图标还会保存，多按几次F5刷新即可


![](https://i.imgur.com/Q8aryf5.png)

---
## 7.文件夹上传以及复制SVN中其他文件夹
SVN地址：http://10.0.204.253/svn/AllResources

1. 空白处右键，或者在已经与SVN关联的文件夹右键
2. ![](https://i.imgur.com/2BTVOzL.png)
3. 会弹出一个SVN的浏览工具，先输入SVN目录地址
4. ![](https://i.imgur.com/GGxGYP3.png)
5. 成功登录后会进入一个SVN浏览器界面
6. ![](https://i.imgur.com/1ei2pTE.png)

### 不拉取他人SVN目录，完成文件夹上传
情景：作为地编人员的我，在自己电脑中创建了一个UE4项目，此时我被要求将此项目上传到DragonMaze中刘畅的文件夹下，但是刘畅的文件夹下已经有200G的项目，我不想拉取他SVN文件夹的情况下，如何将我的UE4项目上传到他的SVN文件夹下？

1. 首先按照以上1~6的操作打开SVN浏览器，找到对应的项目路径，如下
2. ![](https://i.imgur.com/ZkU3wTW.png)
3. 在“刘畅”文件夹上右键，添加文件夹，将本地要上传的文件夹选择即可
3. ![](https://i.imgur.com/qbeCa7w.png)
4. 此时是已经上传成功的界面，在SVN目录中出现了“赌场大厅”的文件夹，本地的“赌场大厅”文件夹与SVN并无关联
4. ![](https://i.imgur.com/1qZqFvc.png)
5. 在不拉取他人SVN目录的情况下便可以完成文件的上传，步骤如上


### 如何安全复制他人SVN文件到自己SVN文件夹
情景：视频同学A，想复制视频同学B的UE4工程文件到自己的目录下，通常情况下直接复制有可能造成引用错乱的问题

1. 可以用以上的操作，将他人的文件夹拉取之后，Add到自己的文件夹下，并且不会引用别人的SVN文件夹关系
