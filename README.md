# taobaoVisitingVenues

## 简介

**双 12 逛会场走起！**

用来（双十一）（双十二）淘宝逛会场来获得喵币的自动化脚本，基于 [auto.js pro 7.0]: https://pro.autojs.org/ 的无障碍服务，for Android 7.0+（auto 8.0 版本把淘宝等 APP 屏蔽了）。理解上和电脑版的按键精灵的区别不大。这里只提供刷猫币的脚本帮助大家远离繁琐的浏览操作（if 能）。同时带上 [hyb1996](https://github.com/hyb1996) 大佬的开源的 free 版的 auto.js，参见这个仓库 [Auto.js]: https://github.com/hyb1996/Auto.js ，里面有相关的使用，有兴趣给这个点个星星哈哈哈，是个超棒的项目呢。

如果嫌 GitHub 下载速度慢，可以去 Gitee 下载 apk。Gitee 的主要的内容都是同步这里的，地址 [taobaoVisitingVenues]: https://gitee.com/sleepybear1113/taobaoVisitingVenues 

12.1 的早上还是个周日，你们就开始催我更新了，恶毒！（手动狗头）

## 目前已知问题

1. 此次双 12 的界面比起双 11 的界面，不是用了控件（也就是说，“充能量”仨字是图片），所以这里只能用绝对坐标进行定位。这里对于 16:9 的手机应该没有大问题，不过小于 3:2 的手机可能存在问题。

2. 逛店到最后会点击猜你喜欢，回到首页。然后可能无法返回领取中心了。此处有点小的瑕疵，可能最后几个逛店要再次运行一下脚本。

## 更新日志

### 1.1.6 12/01 11:00 【脚本在线更新】

1. （改）双 12 更新第一弹，更新双十一脚本为双 12 脚本。

### 1.1.5 11/10 10:20 【脚本在线更新】

1. （改）修复点击“领喵币”打开盖楼结束的提示页面

### 1.1.4 11/05 23:20 【脚本在线更新】

1. （改）较大程度解决浏览店铺出现 5s 广告，进行跳过。5s 广告出现次数很少虽然不影响正常操作，但是还是进行了跳过。

### 1.1.3 11/04 18:45 【脚本在线更新】

1. （改）修复“猜你喜欢”出现同时逛店消失但次数没满，直接去首页的情况（此时可能会增加几次开闭领取中心的次数）

### 1.1.2 11/03 09:50 【脚本在线更新】

1. （改）优化浏览时间的控制，将浏览时间控制在 30s 内（一般在 20s 内），防止手机息屏

### 1.1.1 11/01 22:45 【脚本在线更新】

1. （增）运行中toast提示，增加友好性
2. （增/测试）浏览店铺顺便签到领币（开启方式：“功能选择”中选择第二个）

### 1.1.0 11/01 19:30 【apk 发布】

1. （改）将更新地址改为 Gitee 的 raw。因为 GitHub 的 raw 经常不能访问。
2. （新）解决淘宝浏览某个会场后，返回的时候需要两次
3. （改）每运行 5 次就重新关闭“领取中心”并重新打开
4. （改）将旧代码改得好一些了
5. （重要）需要将本地脚本清除！！！！！！！！
6. （删）将选择功能的选项砍了，虽然悬浮窗的还在，但其实已经没有作用了

### 1.0.6

1. 将去首页浏览猜你喜欢暂时不点击直到全部浏览结束
2. 初版脚本，具体更新情况我也忘记了

## 其他

1. 系统最低要 Android 7.0
2. 第一次开启APP授予权限即可
3. 初始界面是不需要无障碍和悬浮窗的权限，点击开启悬浮窗会
4. 每逢 APP 级别的更新或者安装，执行清除本地脚本
5. APP 里面也有简单的操作介绍
6. 无障碍开启方法:点击悬浮窗启动后转到无障碍设置界面，在里面的应用程序选择这个 APP，开启就OK，不过手机带有悬浮球可能无法开启
7. 开启无障碍后，打开淘宝，转到猫铺界面，最好先把签到做了，然后如果悬浮窗在右侧的挪左边去，然后点击开始就OK了
8. 某些情况下，可能需要比一般的时候更长的时候，比如可能会等待超过 20s，但一般不会超过 35s。一般不提示结束还是在运行的。
9. 结束的标志一般是弹出对话框表示结束，或者就是报了 error 强制停止
10. 关于日志的问题，在脚本 APP 主界面点击返回能看到 log 信息

## 部署问题

### 工具

auto.js pro 7.0.4。现在能看见的只有 free 版的 auto.js 4.0 和收费版的 auto.js pro 8.0。没有 pro 7.0 了。

7.0 和 8.0 的区别就是，8.0 对灰产行业进行了一定的限制，所以对淘宝在内的一些 APP 进行了屏蔽，代码可能在 8.0 上面无法正常运行。

不过也许可以在 free 的 4.0 版部署（不过我没有试过，毕竟我有 pro 7.0 的账号）。

关于 free 版的 auto.js，是个开源项目，参见这个仓库 [Auto.js]: https://github.com/hyb1996/Auto.js ，里面有相关的使用。

### 主要步骤

将 src 里面的代码全部下载，在手机的`/sdcard/`（手机内存）目录建立`脚本/淘宝喵币`目录，将全部的文件移到里面，刷新 auto.js 就能看到新的项目了。（这里感谢[cxgreat2014](https://github.com/cxgreat2014) 指正目录的问题）

如果使用过我这个脚本的话，在手机里面会有“脚本”文件夹，直接用那个就 OK 了。
