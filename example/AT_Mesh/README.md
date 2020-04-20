# AT Mesh 透传

## 简介
AT Mesh透固件块支持Mesh自组网，支持手机传送数据到手机。

## 指令集

|序号|指令|功能|备注|
|----|-----|----|----|
|1|AT|测试AT|
|2|ATE|开关回显|暂未实现
|3|AT+GMR|查询固件版本|
|4|AT+RST|重启模组
|5|AT+SLEEP|深度睡眠|暂未实现
|6|AT+ RESTORE|恢复出厂设置|暂未实现|
|7|AT+BAUD|查询或设置波特率|暂未实现|
|8|AT+NAME|查询或设置蓝牙广播名称|暂未实现|
|9|AT+MAC|设置或查询模组MAC地址|暂未实现|
|10|AT+STATE|查询蓝牙连接状态|暂未实现
|11|AT+ADDR|查询或设置模块的地址|暂时仅支持查询
|12|AT+MESHNAME|查询或设置模块的网络名称|暂时仅支持查询
|13|AT+MESHPWD|查询或设置模块的网络密码|暂时仅支持查询
|14|AT+SEND|A发送数据|
|15|+DATA|收到数据|

## 使用示例

查询模块地址：

    AT+ADDR?
    +ADDR:00a8

发送数据：(向地址为a8的模块发送五个数据，内容为12345)

    AT+SEND:a8,5,12345