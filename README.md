# Mac OS 使用方法：
1. 使用touch命令创建文件corplink-ctrl
```bash
touch corplink-ctrl
```
2. 将文件移入/usr/local/bin
```bash
mv corplink-ctrl /usr/local/bin/
```
3. 添加执行权限
```bash
chmod +x corplink-ctrl
```
4. 启动命令
```bash
sudo corplink-ctrl start
```
5. 停止命令
```bash
sudo corplink-ctrl stop
```
6. 查看状态命令
```bash
sudo corplink-ctrl status
```
7. 关闭开机自启动
##### 创建备份
```bash
sudo cp /Library/LaunchDaemons/com.volcengine.corplink.service.plist /Library/LaunchDaemons/com.volcengine.corplink.service.plist.bak
```
##### 使用默认编辑器打开配置文件
```bash
sudo nano /Library/LaunchDaemons/com.volcengine.corplink.service.plist
```

##### 在文件中找到以下两行并修改为 false,保存文件后重启即可
```xml
<key>RunAtLoad</key>
<false/>
<key>KeepAlive</key>
<false/>
```
