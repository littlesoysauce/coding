# 零基础转CS第一步，架设虚拟机，学习EC2, Linux, SSH技能

大家好，我是小白。许多想转cs的同学不知道怎样迈出第一步，设置专业的编程环境。那么怎样架设一个免费，并且和Amazon, Google之类大厂无缝接轨的工作环境呢？今天小白就来介绍如何通过Amazon Web Services架设属于自己的编程环境。通过这个短视频，你可以学到：
如何在Linux,Mac和windows上使用SSH连接到自己架设的EC2云端服务器。
视频的最后我们一起修改简历，把EC2, SSH等技能写到简历上。

让我们从Amazon EC2开始。 Amazon EC2，全称Elastic Compute Cloud, 也被称为弹性云计算，是AWS提供的云计算服务。

什么是云计算呢？对我们来说云计算就是通过网络连接到远端硬件，当我们想编程的时候，打开电脑连接到EC2服务，就可以在高性能的服务器上运行软件。

那么Elastic是什么意思呢？Elastic是指可扩展的服务。比如说我的项目需要200G的存储空间，可以通过更改EC2参数增加存储空间。

通过这个链接可以注册免费的AWS账户。
注册成功以后，可以看到AWS管理控制台，使用Services下拉菜单, 在Compute部分下找到EC2服务。首先单击左侧导航窗格上的Instances，然后单击Launch Instance按钮。我们看到一些Amazon Machine Image可以选择。这决定了服务器的操作系统，Red hat是一种业界通用的linux操作系统，我们选它。
剩下的参数不做更改，我们直接选择Review and Launch。可以看到AWS为我们配置了1G内存的单核CPU.
了解服务器性能后，点击Launch按钮。接下来必须选择一个密钥对。如果说服务器的认证系统是大门的话，密钥对就是打开大门的钥匙。
输入你的密钥文件的名称，把密钥对下载到本地。密钥对在将来登陆EC2服务器会用到，选择确认启动EC2服务器。

等待一会,我们已经可以连接到服务器了。我们先来演示windows用户用ssh工具连接到EC2服务器。ssh是用来远程连接服务器的程序和协议。

连接到服务器我们需要一个有ssh功能的客户端。如果你是windows用户，推荐使用MobaXTerm,可以在官网上免费下载。

打开Xterm以后选择右键新建Session, 选择ssh作为连接方式，我们需要回到EC2 console复制服务器的ip地址作为remote host

在advanced SSH setting选项卡里选择使用private key,并且找到key文件。
点击确认连接到远端服务器。注意用户名必须输入ec2-user才能登陆。输入用户名客户端就会用我们的private key登录服务器。
这就是在windows下通过ssh客户端登录远程服务器的方法，如果你有问题可以给我留言。

接下来我们将在mac和Linux系统下用ssh登陆服务器。mac和linux操作系统都自带了ssh命令，所以我们放在一起讲。
首先介绍三个linux系统下的命令，pwd可以查询当前路径，cd x用来把当前路径改为x，chmod更改文件访问权限。
我们需要通过chmod命令更改private key的访问权限。再通过ssh命令远程连接到ec2服务器。  

找到private key之后通过chmod命令将private key的访问权限变为只允许私人访问。
在通过ssh命令链接到远端服务器。


这就是在max和linux中通过ssh链接到ec2服务器的方法。现在我们打开简历模板修改简历。
大家可以看到技能被份类成了留个模块，Linux, Mac和Windows属于操作平台。而EC2和SSH属于开发工具。


好了，这就是关于架设EC2服务器的方法，如果你有任何问题，可以在评论区里给我留言，我会尽快回答。
下一个视频我会交大家如何设置Python环境，学习github, yum, python技能。 
如果你喜欢这个视频请按赞鼓励，下次再见咯。


