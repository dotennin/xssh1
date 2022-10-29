# xssh

仅仅需要一个GitHub账号即可！不过这个账号不能是qq邮箱注册的，这个后缀不行。如果你正好是qq注册的，可以在GitHub后台添加个gmail邮箱，并且把原来的删除即可。小提示：如果你网络无法访问GitHub，看看<https://iweec.com/381.html>

开始操作：

一、打开页面：<https://github.com/MetaVPS/xssh1> 直接登录，创建一个分支，库名称保持xssh；

二、打开页面：<https://dashboard.ngrok.com/login> 直接使用GitHub账号登录，然后在入门中找到授权令牌如图：

![授权令牌.PNG](https://iweec.com/usr/uploads/2022/07/3970998153.png "授权令牌.PNG")

三、在你自己仓库中修改config.sh,内容为 NGROK_TOKEN="这里粘贴你的令牌"，然后返回仓库，拷贝仓库地址，格式例如：[https://github.com/你的名字/xssh](https://github.com/%E4%BD%A0%E7%9A%84%E5%90%8D%E5%AD%97/xssh)

四、打开页面：<https://cloud.okteto.com/#/login> 同样用GitHub登录，然后在左上角点击：新建开发环境------git方法------url获取，填写上一个步骤中你的xssh URL，分支填写 main，然后启动。稍等1-3分钟，直到网络部署显示运行！\
![网络部署.PNG](https://iweec.com/usr/uploads/2022/07/2333084373.png "网络部署.PNG")

五、我们回到ngrok，在端点或者隧道代理中可以看到，类似 tcp://2.tcp.ngrok.io:12795 这样的一个地址。

这样就可以了，接下来我们进行ssh连接，你的用户名和密码和我保持一致，地址和端口要看你自己的后台哦：

地址：2.tcp.ngrok.io\
端口：12795\
用户名：root\
密码：majalaya

连接成功，我查看了一下htop，哇哦4核32G！！

![htop.PNG](https://iweec.com/usr/uploads/2022/07/1783722128.png "htop.PNG")

ngrok和okteto的网页关闭后，机器仍然能运行，我也简单测试了两个脚本，能跑。

免责声明：此文包括视频内容为原创，在制作中参考了一些网络内容，感谢GitHub、ngrok和okteto以及majalaya！

更多的问题请看这里：

vps能用多久？未知，我只用了半个小时测一下就关闭了，理论上永久，而且可以重装；

安全吗？不知道，这是由亚马逊提供的美国实例，不是我的，想保存重要文件肯定不行，玩玩而已吧；

能搭建代理吗？ 额，我建议你用这个实例来学习Linux系统，如果仅仅搭建代理，ngrok或者okteto都可以胜任。

当然你要是需要更高级的功能，我也支持你购买ngrok和okteto。
