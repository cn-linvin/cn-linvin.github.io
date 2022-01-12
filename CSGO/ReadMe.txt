cmd：
reg add HKLM\System\CurrentControlSet\Control\Power /v PlatformAoAcOverride /t REG_DWORD /d 0
powercfg -duplicatescheme e9a42b02-d5df-448d-aa00-03f14749eb61
bcdedit /set useplatformclock no
bcdedit /set useplatformtick yes
bcdedit /set disabledynamictick yes

WIN+R，regedit：
计算机\HKEY_CURRENT_USER\Control Panel\Keyboard
    修改KeyboardDelay为0
    修改KeyboardSpeed为48
计算机\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Power\PowerSettings\0012ee47-9041-4b5d-9b77-535fba8b1442\51dea550-bb38-4bc4-991b-eacf37be5ec8
    修改ValueMax为0
    修改ValueMin为0
计算机\HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Control\GraphicsDrivers\Configuration
    查找Scaling，修改Scaling为3

NVIDIA控制面板：
缩放全屏
通过预览调整图像设置->使用我的优先选择->侧重于性能->应用
管理3D设置->恢复->高性能NVIDIA处理器->低延时模式(超高)->纹理过滤-负LOD偏移(锁定)->纹理过滤-质量(高性能)->应用

系统：
显示->图形设置->开->浏览->csgo.exe->选项->高性能
声音->声音控制面板->耳机->属性->高级->2通道,16位,44100Hz
电源和睡眠->其他电源设置->卓越性能->选择电源按钮的功能->更改当前不可用的设置->取消启用快速启动

游戏：
关闭Xbox Game Bar
关闭屏幕截图
开启游戏模式

轻松使用：
关闭键盘

启动选项：
+exec 1 -tickrate 128

1.cfg：
...\steamapps\common\Counter-Strike Global Offensive\csgo\cfg
exec 1

video.txt：
...\userdata\1246918298\730\local\cfg

本地文件：
浏览->csgo.exe->属性->兼容性->勾选禁用全屏优化
浏览->csgo.exe->属性->兼容性->更改高DPI设置->勾选替代高DPI缩放行为(应用程序)
验证游戏文件的完整性

ISLC（cmd：lodctr /r）：
Free memory is lower than: 8192（内存/2）
勾选Start ISLC minimized and auto-Start monitoring.
勾选Launch ISLC on user logon. (TaskScheduler)
Wanted timer resolution: 0.50
勾选Enable custom timer resolution
Start

WiFi：
控制面板->网络和 Internet->网络连接->WLAN->属性 ->配置->高级->首选频带->5GHz

热点：
控制面板->网络和 Internet->网络连接->本地连接*10->属性->配置->电源管理->取消允许计算机关闭此设备以节约电源

设备管理器：
磁盘驱动器->属性->策略->取消启用设备上的写入缓存
通用串行总线控制器->USB根集线器->属性->电源管理->取消允许计算机关闭此设备以节约电源

重启

---

退出：
WeChat.exe

死亡竞技：
sv_cheats 1;bot_kick;mp_roundtime 60;mp_restartgame 1;sv_cheats 0;

demo:
playdemo ...\steamapps\common\Counter-Strike Global Offensive\csgo\?
demoui