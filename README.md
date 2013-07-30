##一些说明

昨天在硬盘上划出一块新分区安装了Ubuntu 13.04，但是对原来用wubi安装在win7下的Ubuntu的备份似乎无法直接应用在这个新装的系统上面……于是许多软件又要重新装了，但问题在于我忘记了很多原来装的软件以及一些软件安装的方法……这次又要慢慢来了，真是麻烦啊  
所以呢，我打算将在本系统中安装各种软件的过程记录下来……以备后用……  
—— FJL 2013.07.30

-------------
####13.07.30
###init

之前备份了/etc/apt/sources.list   
用了以下方法备份了软件安装列表，这回先按照此法恢复了，但是不全……  
backup: 

	$ sudo dpkg --get-selections > my_installed_base  
recover:   

	$ sudo dpkg --set-selections < my_installed_base  
	$ sudo apt-get dselect-upgrade  
另外，导入源之后update出现找不到公钥的情况，经观察错误信息中的网址在[此处](http://www.tolaris.com/apt-repository/)找到了解决方法  

###sublime text 2

	$ sudo add-apt-repository ppa:webupd8team/sublime-text-2  
	$ sudo apt-get update  
	$ sudo apt-get install sublime-text  
[参考](http://yishanhe.net/sublime-text-2-ubuntu-ppa/)  

###git

	$ sudo apt-get install git  

###build-essential
	$ sudo apt-get install build-essential  

-----------------------------