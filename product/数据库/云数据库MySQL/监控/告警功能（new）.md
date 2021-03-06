您可以创建告警用于在云产品状态改变时触发警报并发送相关消息。创建的告警会根据每隔一段时间监控的指标相对于给定阈值的情况判断是否需要触发相关通知。
状态改变触发告警后，您可以及时进行相应的预防或补救措施。因此，合理地创建告警能帮助您提高应用程序的健壮性和可靠性。有关告警的更多信息，请参考 [创建告警][1]。

## 创建告警策略
1. 登录 [腾讯云控制台][2]，单击【云监控】>【我的告警】选项卡，单击【告警策略】菜单，在告警策略列表页上单击【新增告警策略】按钮。
![](//mc.qcloudimg.com/static/img/860d49c84c83a4271b90767a5cbf89ef/image.png)
![](//mc.qcloudimg.com/static/img/12704bae3992fd2cedee31ba89071c2a/image.png)
2. 在新增告警策略弹出框中，输入策略名称、选择策略类型（要作用的产品）并选择告警触发条件。
告警触发条件是指标、比较关系、阈值、统计周期和持续周期组成的一个有语义的条件。例如：指标为 【磁盘使用率】 、比较关系为【>】 、阈值为 【80%】、统计周期为【5 分钟】、持续周期为【2 个周期】，表示：每 5 分钟收集一次磁盘使用率数据，若某台云数据库的【磁盘使用率】连续两次大于 80% 则触发告警。单击【下一步：关联告警对象】
![](//mc.qcloudimg.com/static/img/fc3830b9c4910feb7a08da76c64098e2/image.png)
3. 选择您需要关联对象所在的地域或者通过对象的实例 ID 进行搜索，勾选需要关联的对象实例，单击【下一步：设置接收组】。
![](//mc.qcloudimg.com/static/img/7a7fbad0bc58f746c6ee410fcb2034f3/image.png)
4. 选择【告警接收组】后，单击【完成】。

## 关联对象

1. 登录 [腾讯云控制台][3]，单击【云监控】>【我的告警】选项卡，单击【告警策略】菜单。在告警策略列表页中，单击刚刚创建的告警策略，在详情页中单击【新增关联】。![](//mc.qcloudimg.com/static/img/a34ebce6478c8b40d3194161fd85a830/image.png)
2. 选择您需要关注的云产品，单击【应用】按钮。
![](//mc.qcloudimg.com/static/img/2e7b0fd3a6c3b53b29f2c9665f1925f2/image.png)

## 设置接收告警的对象

1. 登录[腾讯云控制台][4]，单击【云监控】>【我的告警】选项卡，单击【告警策略】菜单。在告警策略列表页中，单击已经创建的告警策略，在详情页中单击【管理告警接收组】
![](//mc.qcloudimg.com/static/img/a8c1dd33a761c4758d5bd203242b7f04/image.png)
2. 勾选需要通知的用户组，单击【保存】。
![](//mc.qcloudimg.com/static/img/e33bb450c694a5672050ab70d0ad8b0a/image.png)。

每个告警策略是一系列告警触发条件的集合，告警触发条件是“或”关系，即一个条件满足，就会发送告警。告警将发送至告警策略关联的所有人，用户接收到告警后可以及时查看并采取相应措施。

[1]:	https://www.qcloud.com/doc/product/248/1073
[2]:	https://console.qcloud.com/
[3]:	https://console.qcloud.com/
[4]:	https://console.qcloud.com/
