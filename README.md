# Mac OS 使用方法：
#使用touch命令创建文件corplink-ctrl
touch corplink-ctrl
#将文件移入/usr/local/bin
mv corplink-ctrl /usr/local/bin/
#添加执行权限
chmod +x corplink-ctrl
#启动命令
sudo corplink-ctrl start
#停止命令
sudo corplink-ctrl stop
#查看状态命令
sudo corplink-ctrl status

#关闭开机自启动
#创建备份
sudo cp /Library/LaunchDaemons/com.volcengine.corplink.service.plist /Library/LaunchDaemons/com.volcengine.corplink.service.plist.bak

# 使用默认编辑器打开配置文件
sudo nano /Library/LaunchDaemons/com.volcengine.corplink.service.plist

#在文件中找到以下两行并修改为 false：
<key>RunAtLoad</key>
<false/>

<key>KeepAlive</key>
<false/>
#保存文件后重启即可
