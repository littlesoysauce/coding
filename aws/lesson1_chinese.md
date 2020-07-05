# 零基础转CS第一步，架设虚拟机，学习EC2, Linux, SSH技能

大家好，我是小白。许多想转cs的同学不知道怎样迈出第一步，设置专业的编程环境。那么怎样架设一个免费，并且和Amazon, Google之类大厂无缝接轨的工作环境呢？今天小白就来介绍如何通过Amazon Web Services架设属于自己的编程环境。通过这个短视频，你可以学到：
如何在Linux,Mac和windows上使用SSH连接到自己架设的EC2云端服务器。
视频的最后我们一起修改简历，把EC2, SSH等技能写到简历上。

让我们从Amazon EC2开始。 Amazon EC2，全称Elastic Compute Cloud, 也被称为弹性云计算，是AWS提供的云计算服务。

什么是云计算呢？对我们来说云计算就是通过网络连接到远端硬件，当我们想编程的时候，打开电脑连接到EC2服务，就可以在高性能的服务器上运行软件。

那么Elastic是什么意思呢？Elastic是指可扩展的服务。比如说我的项目需要200G的存储空间，可以通过更改EC2参数增加存储空间。

通过这个链接可以注册免费的AWS账户。
注册成功以后，可以看到AWS管理控制台，我将使用Services下拉菜单, 在Compute部分下到EC2服务。首先单击左侧导航窗格上的Instances，然后单击Launch Instance按钮。我们看到一些Amazon Machine Image可以选择。这决定了服务器的操作系统，Red hat是一种业界通用的linux操作系统，我们选它。
剩下的参数不做更改，我们直接选择Review and Launch。可以看到AWS为我们配置了1G内存的单核CPU.
接下来必须选择一个密钥对。如果说服务器的认证系统是大门的话，密钥对就是打开大门的钥匙。把密钥对下载到本地。

输入你的密钥文件的名称，再勾选方框，确认必须拥有密钥对才能登陆EC2服务器，选择确认启动EC2服务器。

等待一会,我们已经可以连接到服务器了。我们先来演示windows用户用ssh工具连接到EC2服务器。ssh是用来远程连接服务器的程序和协议。

连接到服务器我们需要一个有ssh功能的客户端。如果你是windows用户，推荐使用MobaXTerm,可以在官网上免费下载。

打开Xterm以后选择右键新建Session, 选择ssh, 在advanced SSH setting里选择使用private key,并且找到key文件。注意这里的用户名必须是ec2-user才能登陆。
第一次登陆以后就可以把登陆信息记录在系统里，接下来就可以随时创建一个session登陆了。

接下来我们展示怎样用在mac和Linux系统下用ssh登陆服务器。因为mac和linux操作系统都自带了ssh命令，所以登陆方式是一样的。

最后通过ssh命令远程连接到ec2服务器。
ssh -i "test1.pem" ec2-user@ec2-18-191-134-53.us-east-2.compute.amazonaws.com。
命令行中表达了private key文件，用户名和远端服务器的ip地址。

这就是架设远程服务器的方法。现在我们打开简历模板。
在简历技能一项里，在development一项加入EC2和SSH
在Platform加入操作系统Linux, Mac和Windows

好了，这就是关于架设EC2服务器的方法，如果你有任何问题，可以在评论区里给我留言，我会尽快回答。
下一个视频我会交大家如何设置Python环境，学习github, yum, python技能。 
如果你喜欢这个视频请按赞鼓励，下次再见咯。


