# esxi6.7u3P8_UI_fix

****修复esxi 6.7u3 20221004001（Build 20497097）Host Client（浏览器）无法添加vmdk的bug****

![_~41U0~P5NG$BB7~2(V2N2S](https://github.com/tujj99/esxi6.7u3P8_UI_fix/assets/53027340/808ce53e-0ba7-485b-b470-4647161a8b27)

解决办法：

1、降级esx-ui版本到前一个版本。

操作步骤：

1、打开esxi的ssh、tsm-ssh

2、下载VMware_bootbank_esx-ui_1.33.7-15803439.vib到esxi任意目录

3、移除原有ui

``esxcli software vib remove -n esx-ui  ``

4、安装旧ui

``esxcli software vib install -v /VMware_bootbank_esx-ui_1.43.10-20199807.vib``

不用重启，ui替换完即时生效

ps：官网得加油了，这么久还不修复这个bug
