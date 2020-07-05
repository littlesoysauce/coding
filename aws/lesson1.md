# AWS free tier
https://aws.amazon.com/free/


# What is Amazon EC2
* Known as Elastic Compute Cloud.
* Provides on-demand, scalable compute capacity in the AWS cloud
* The compute instances are known as EC2 Instance

Let's start by talking about what is Amazon EC2. Amazon EC2, also known as Elastic Compute Cloud, is the compute offering from AWS. It provides on-demand, scalable compute capacity in the AWS cloud.
让我从讨论什么是Amazon EC2开始。 Amazon EC2， 也被称为弹性云计算，是AWS提供的云计算服务。他在AWS云中提供
按需的，可伸缩的计算能力。

* Allows various configurations of CPU, memory, storage and networking capabilities.
* Instances can be launched in multiple regions
* Also referred to as IaaS(Infrastructure as a Service)
Think of virtual machines that you may have provisioned on your local machine, by installing a hypervisor. Now move these virtual machiens to the AWS cloud, and these are now called as EC2 isntnances. So EC2 Instances are virtual machines that you launch in the AWS cloud. It allows various configurations of CPU, memory, storage and networking capabilities, and these configurations are available as pre-defined out-of-the-box configurations when you launch an EC2 Instance.
通过安装管理程序，可以在本地机器上配置虚拟机。现在将这些虚拟机移动到AWS云，这些虚拟机现在成为EC2实例。因此，EC2实例是您在AWS云中启动的虚拟机。它允许CPU，内存，存储和网络功能的各种配置。当您启动EC2实例时，这些配置可作为预定义的开箱即用配置系统。


 
For example, I can launch an EC2 Instance that provides one virtual CPU and one GB of RAM, or maybe four virtual CPUs and eight GB of RAM. These configurations are readily available. All we need to do is select any one of these configurations and launch an EC2 instnace. These Instances can be launched in multiple regions. Any region where AWS provides a service can be used to launch an EC2 Instance. I could be the closest region to you, or maybe the most cost-effective region, or maybe the region that helps you the most with your compliance requirements. 

例如，我可以启动一个EC2实例，它提供一个虚拟CPU和一个GB的RAM，或者可能提供四个虚拟CPU和八个GB的RAM。 这些配置很容易获得。 我们所需要做的就是选择这些配置中的任何一种，并启动EC2安装。 这些实例可在多个区域启动。 AWS提供服务的任何区域都可以用来启动EC2实例。 我可能是最接近你的区域，或者可能是最具成本效益的区域，或者可能是帮助你最符合你的合规要求的区域

Amazon EC2 is also referred to as IaaS, also known as Infrastructure as a Service. When you launch a virtual machine using Amazon EC2, you have complete control over the operating system that's running on the EC2 Instance, and any applications that you install on top of it. So you can use the EC2 Instance as an application server, a database server, or maybe as a batch-processing server. The entire infrastructure is provided to you, and it's in your control. 

Amazon EC2也成为IaaS，也成为基础设施服务。当你使用Amazon EC2启动虚拟机时，可以完全控制运行在EC2实例上的操作系统，以及安装在其上的任何应用程序。因此，你可以将EC2实例用作应用程序服务器，数据库服务器，或批处理服务器。整个基础设施都提供给你，你可以控制它。


#Key Features
* Low cost
* Quickly scalable(up or down)
* Complete control
* No upfront investment
* Multiple locations
Let's look at the key features that makes Amazon EC2 such a popular offering. At the top of the list is low cost. Amazon EC2 Instances are launched using shared hardware. In the background, AWS uses physical servers and the capacity of these physical servers is shared by multiple customers in the form of EC2 instnaces.
让我们看看让Amazon EC2成为如此受欢迎产品的关键特性。最重要的是低成本。Amazon EC2多个实例在后台共享硬件驱动。在后台，AWS使用物理服务器，这些武力服务器的容量由多个客户以EC2实例的形式共享。

Because the configuration and capacity is shared, the cost is split up as well, making Amazon EC2 an incredibly low-cost offering. It is quickly scalable, both up and own. Let's say I launch an EC2 instance with two virtual CPUs and four GB of RAM, and I quicly realize that I need more capacity to serve my customers. All I need to do is shut down the EC2 Instance, change the configuration, and reboot it. Now in a matter of few minutes, I have more capacity. The opposite is true, as well. Let's say I have an EC2 instnace with a lot of idle capacity. I can quickly scale it down to save my cost. Next, you have complete cotnrol over the EC2 instance. There is no upfront investment, it has a pay-as-you-go model. Though AWS provides an offering called as reserve EC2 instances, which allows you to make an upfront payment to receive billing discounts, we don't really have to. We can simply launch an EC2 Instnace, and choose to use the pay-as-you-go model. Finally, EC2 instances can be launched in any of the regions where AWS provided its services.

由于配置和容量是共享的，所以成本也被分割，这使得Amazon EC2成为了一款低得令人难以置信的产品。它具有快速的可扩展性。假设我启动了一个带有两个虚拟cpu和4 GB RAM的EC2实例，我很快意识到我需要更多的容量来服务我的客户。我所需要做的就是关闭EC2实例、更改配置并重新启动它。几分钟后，我的容量增加了。反之亦然。假设我有一个EC2 instnace有很多空闲容量。我可以迅速缩小规模以节省成本。接下来，在EC2实例上完成cotnrol。它没有前期投资，而是采用现收现付模式。尽管AWS提供了一个名为EC2 reserve instances的服务，允许您预付预付款以获得账单折扣，但我们真的不必这样做。我们可以简单地启动EC2 Instnace，并选择使用现收现付模型。最后，可以在AWS提供服务的任何区域启动EC2实例。

I am here at the AWS Management console, I will use the Services dropdown and navigate to the EC2 service, which can be found under the Compute section. I have a notice at the top that talks about the new EC2 console. By the time you watch this video, you may have the new EC2 console active on your account. The steps may change a bit, but the components that make up the EC2 instance are going to remain the same. I will start by clicking on instances on the left navigation pane, and then click the Launch Instance button. You will notice there are seven steps in launching an EC2 instance. The first step is to choose an Amazon machine image. The Amazon machine image identifies the operating system that will be installed on the EC2 instance. So that's our first component, an AMI.

我现在在AWS管理控制台，我将使用Services下拉菜单并导航到EC2服务，他可以在Compute部分找到。首先单击左侧导航窗格上的Instances，然后单击Launch Instance按钮。你将逐一到启动EC2实例有七个步骤。第一步是选择一个Amazon机器映像。Amazon机器映像决定了EC2实例的操作系统。这是我们的第一个组件，AMI.

Over here I have a list of predefined AMIs. For this demonstration I will select the first one. On step two need to select an instance type. An instance type describes the size of the EC2 instance, meaning the configuration or the capacity of the EC2 instance. So here we have the different families of EC2 instances. Here we have the types. By default, it selects the T2 microsize, which provides one virtual CPU, and one GB of RAM. So that's the second component involved in launching an EC2 instance, instance type.

在这里我有系列预定义的ami。对于这个演示，我将选择第一个。在步骤2中，需要选择实例类型。实例类型描述了EC2实例的大小，即EC2实例的配置或容量。这里我们有不同种类的EC2实例。这里我们有类型。默认情况下，它选择免费的T2型，它提供一个虚拟CPU和一个1GB的RAM。这是启动EC2实例的第二个组件，实例类型。
ex. Windows, 操作系统和软件, ie, microsoft word, ppt

Let's move to the third step. On step number three, there's a variety of configuraiton that we can specify. For example, we can define the network, the subnet, do we want a public IP, do we want to place this instance into a placement group? Do you want to attach an IAM role? Do we want to enable detailed monitoring, tendency, and user data that we can specify? So there's a lot of configuration that we can make on step number three.
让我们进入第三步。在第三步，我们可以指定各种设定。例如，我们可以定义网络，子网，是否需要公共IP，是否要将此实例放到放置组中?你是否要设置IAM权限?我们是否需要启用详细的监测趋势和用户数据工具?所以在第三步我们可以设置许多参数。

Let's move to step four. Remember, we are just trying to identify the components that make up an EC2 instance,so we can spend time understanding each of these components in detail. Step four is about storage. By default it has a root volume, on which the operating system will be installed. It has a specific type and we can change the type, and we can also add additional volumes. Think of this as a hard disk that you would attach to a physical laptop.

让我们进入第四步。请记住，我们只是试图识别组成EC2实例的组件，因此我们可以花时间详细了解每个组件。第四步是关于存储。默认情况下，它有一个根卷，操作系统将安装在根卷上。它有一个特定的类型，我们可以改变类型，我们也可以增加额外的体积。可以把它看作是一个硬盘，可以连接到物理笔记本电脑上。

By default, it attaches a root volume, which will be used to install the opearting system. THi sis the name of the Device and this is the snapshot id. The snapshot ID is used to identify the backup for this volume. Here we hae the Size of the volume and then we have the Volum Type. Different volume types are used for different use cases. Next, we have the IOPS, or input/output per second. Throughput is another metric that is used to measure the perforamnce of a volume, but it is only applicable to specific volume types. Next, we have Delete on Termination and by default, the checkbox is turned on, which means, if you terminate the EC2 instance, the EBS volume will be deleted. But, if I uncheck this box, even if you terminate yoru EC2 instance, the EBS volume will continue to exist. And for this volume, we do not have encryption turned on.


On the next step we can add tags. Tags are labels that you can attach to your EC2 instance, for identification purpose. 

下一步我们可以添加标记。标签是可以附加到EC2实例的标签，用于标识。

Moving to step number six, we need to configure a security group. A security group is a set of firewall rules that controls the traffic for your EC2 instance. By default, it creates a new security group or we can select an existing security group if we have one configured from earlier. Security group is a very important component of an EC2 instance.

转到步骤6，我们需要配置一个安全组。安全组是一组防火墙规则，用于控制EC2实例的通信。默认情况下，它会创建一个新的安全组，或者我们可以选择一个现有的安全组(如果之前配置了一个安全组)。安全组是EC2实例的一个非常重要的组件。

Fianlly, I will click Review and Launch. This shows all the settings that I've selected, and when I click the Launch button, I can select a Key Pair. A Key Pair is used to log into an EC2 instance. So there are several components that make up an EC2 instance. Before we go ahead and launch the EC2 instance, it is imp;ortatn that we understand every component in detail. 
最后，我会点击查看和启动。这显示了我选择的所有设置，当我单击Launch按钮时，我可以选择一个密钥对。密钥对用于登录到EC2实例。所以有几个组成EC2实例的组件。





