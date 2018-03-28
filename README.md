# ios_LaunchDaemons
文件在手机中的目录：/System/Library/LaunchDaemon

| 目录 | 用途 |
| --- | --- |
| /System/Library/LaunchDaemons | 存放属于系统本身的守护程序plist文件 |
| /Library/LaunchDaemons | 存放第三方程序的守护程序plist文件 |
| /System/Library/LaunchAgents | 存放属于系统本身的代理程序plist文件 |
| /Library/LaunchAgents | 存放第三方程序的代理程序plist文件，通常为空 |
| ~/Library/LaunchAgents | 用户自有的launch代理程序，只有对应的用户才会执行。 | | 用户自有的launch代理程序，只有对应的用户才会执行。 |
    
    
    
    

# 文件含义
<font color=green>* 删除后没有影响的开机启动项:
> com.apple.aslmanager.plist........................管理系统日志的进程
> com.apple.chud.chum.plist.........................关于CHUD(硬件开发)的进程
> com.apple.chud.pilotfish.plist......................关于CHUD(硬件开发)的进程
> com.apple.CrashHouseKeeping.plist..........这个也是关于崩溃的进程
> com.apple.DumpBasebandCrash.plist........记录基带崩溃信息的进程(无SIM卡插槽的设备没有)
> com.apple.DumpPanic.plist.........................记录系统崩溃信息的进程
> com.apple.powerlog.plist.............................监视第三方不被苹果设备兼容的充电器的进程
> com.apple.ReportCrash.[XXXXXX].plist........共有N多以[com.apple.ReportCrash]开头的文件,记录软件崩溃原因和时间的进程
> com.apple.syslogd.plist...............................记录系统日志的进程
> com.apple.mobile.profile_janitor.plist..........未知作用的进程,删除无影响
> com.apple.iqagent.plist...............................未知作用的进程,删除无影响
> com.apple.stackshot.server.plist.................未知作用的进程,删除无影响com.apple.tcpdump.server.plist..................可能是用来转存网络数据的,具体功能未知,删除无影响</font>

<font color=orange>* 删除后禁用部分功能的启动项:
> com.apple.searchd.plist...............................启用Sportlight(桌面最左面那个搜索器)搜索功能的进程
> com.apple.accessoryd.plist..........................启用配件支持的进程(使用底座、音响的用户删完后会杯具)
> com.apple.apsd.plist....................................启用Push邮件通知功能(在天朝比较很少用)
> com.apple.iapd.plist.....................................启用配件支持的进程(使用底座、音响的用户删完后会杯具)
> com.apple.dataaccess.dataaccessd.plist.....通过Excahge或Google同步的进程(用Excahge或Google同步的用户不要删)
> com.apple.datamigrator.plist........................启用将SIM卡上的联系信息存到3G版iPad和iPhone上的进程(对无SIM卡插槽的设备来说是累赘)
> com.apple.racoon.plist.................................启用Vρ∩的进程(用Vρ∩Da1L1上Twitter、Facebook、Google+、YouTube的用户请不要删除)
> com.apple.MobileInternetSharing.plist.........启用共享上网服务(对无SIM卡插槽的设备来说是累赘)
> com.apple.AOSNotification.plist...................启用MobileMe同步功能的进程(使用MobileMe同步功能请勿删除)
> com.apple.AdminLite.plist............................自动关闭崩溃软件的进程
> com.apple.mobile.obliteration.plist...............删除用户数据的进程(删除后禁用恢复出厂设置、密码错误删除、远程抹掉用户信息功能)
> com.apple.scrod.plist...................................启用语音控制的进程
> com.apple.itunesstored.plist........................这个进程不能完全禁用,否则你就不能使用AppStore来安装程序据说</font>

<font color=red>* 绝不能删除的关键开机启动项:
> com.apple.fairplayd.plist..............................启动数字权限管理的进程(删了就完了)
> com.apple.installd.plist.................................启动容许安装软件的进程
> com.apple.BTServer.plist.............................未知进程(删了后,速度会变成[超慢])
> com.apple.configd+pm.plist..........................系统设置
> com.apple.configd-pm.plist...........................系统设置
> com.apple.gmmd.plist...................................调试进程
> com.apple.mDNSResponder.plist.................DNS进程
> com.apple.mDNSResponderHelper.plist.......DNS进程
> com.apple.mediaserverd.plist.......................播放音乐和视频的进程
> com.apple.usbptpd.plist................................使你的机器插上电脑后充电
> com.apple.mtmergeprops.plist......................触摸控制进程
> com.apple.SCHelper-embedded.plist...........系统设置
> com.apple.SpringBoard.plist........................启动springboard的进程
> com.apple.mobile.Lockdown.plist.................启动SIM网络的进程(不管有没有SIM卡,都不要删)
> com.apple.itdbprep.plist...............................同步音乐的进程
> com.apple.locationd.plist.............................启用定位的进程</font>



> com.apple.ABDatabaseDoctor.plist -通讯录数据库诊断，删除无影响，还可以防止苹果窃取用户通讯录
> 
> com.apple.absd.plist -siri相关
> 
> com.apple.accountsd.plist -添加邮件帐户启动项，删除可能会造成卡顿或无法开机，绝对不可以删除
> 
> com.apple.adid.plist -会导致appstore无法安装应用，不可删除
> 
> com.apple.afcd.plist -无法用afc2add插件，不可删除
> 
> com.apple.aggregated.addaily.plist -用于生成对应功能的日志，直接删除
> 
> com.apple.aggregated.plist -电量使用情况相关，删除后将不显示各个应用程序使用电池的百分比，不需要这个功能的可以删除
> 
> com.apple.ait.aitd.plist -未知，不建议删除。但是我删除了暂无影响
> 
> com.apple.AOSNotification.plist -未知，我删除了暂无影响
> 
> com.apple.appsupport.cplogd.plist -用于生成日志，直接删除
> 
> com.apple.apsd.plist -推送服务，不可删除
> 
> com.apple.askpermissiond.plist -未知，我删除了暂无影响
> 
> com.apple.aslmanager.plist -用于管理日志，直接删除
> 
> com.apple.assertiond.plist -和Siri，和第三方输入法相关
> 
> com.apple.AssetCacheLocatorService.plist -相机缓存位置服务相关，删除暂无影响
> 
> com.apple.assetsd.nebulad.plist -貌似相机照片相关，但是删除了暂无影响
> 
> com.apple.assetsd.plist - 相机相关
> 
> com.apple.assistantd.plist -辅助，可能和siri相关
> 
> com.apple.assistant_service.plist -同上
> 
> com.apple.assistivetouchd.plist -著名的小圆点
> 
> com.apple.atc.atwakeup.plist - 据说和iTunes同步有关，但是我不用iTunes同步，所以删除了
> 
> com.apple.atc.plist  -同上
> 
> com.apple.awdd.plist -日志相关，果断删除
> 
> <font color=red>com.apple.backboardd.plist - 核心进程，springboard 必备</font>
> 
> com.apple.backupd.plist -和iTunes备份相关，我是从不用，所以删了
> 
> com.apple.bird.plist -IOS8新功能，未知，我删除了暂无影响
> 
> com.apple.BlueTool.plist -以下和蓝牙相关
> 
> com.apple.BTServer.avrcp.plist
> 
> com.apple.BTServer.le.plist
> 
> com.apple.BTServer.map.plist
> 
> com.apple.BTServer.pbap.plist
> 
> com.apple.BTServer.plist
> 
> com.apple.cache_delete.plist -IOS8新功能，貌似删除缓存用的，不建议删除
> 
> com.apple.calaccessd.plist -日历相关，不建议删除
> 
> com.apple.CallHistorySyncHelper.plist -IOS8新功能，字面意思是呼叫历史同步帮助，我删除了暂无影响
> 
> com.apple.certui.relay.plist -当你在一个公共网络，safari无法校验一个网站时，会提示这个网站未经过验证，是否继续。我直接删除了
> 
> com.apple.cfnetwork.AuthBrokerAgent.plist -可能还是什么网络验证，我直接删除了，暂无影响
> 
> com.apple.cfnetwork.cfnetworkagent.plist -同上
> 
> <font color=red>com.apple.cfprefsd.xpc.daemon.plist -IOS8新功能，删除后要重新激活，亲测，切不可删除！</font>
> 
> com.apple.cloudd.plist -云服务，我从不用，直接删除了
> 
> com.apple.cloudphotod.plist -云照片，同上
> 
> com.apple.cmfsyncagent.plist -未知，我删除了无影响
> 
> <font color=red>com.apple.CommCenter.plist -以下为通信功能，切不可删除</font>
> 
> com.apple.CommCenterClassic.plist
> 
> com.apple.CommCenterLite.plist
> 
> com.apple.CommCenterMobileHelper.plist -删除后设置-运营商将显示为英文，但是不影响任何功能
> 
> com.apple.CommCenterRootHelper.plist -删除后可以打电话，但是无法用手机卡上网
> 
> <font color=red>com.apple.configd.plist -核心进程，删除后白苹果，连SSH都无法使用</font>
> 
> com.apple.containermanagerd.plist -容积管理，删除后无法安装软件，亲测，切不可删除！
> 
> com.apple.CoreAuthentication.daemon.plist -IOS8新功能，我删除了暂时无影响
> 
> com.apple.corecaptured.plist -未知，我删除了暂无影响
> 
> com.apple.coreduetd.plist -未知，我删除了暂无影响
> 
> com.apple.corercd.plist -未知，我删除了暂无影响
> 
> com.apple.coreservices.appleid.authentication.plist -苹果id验证
> 
> com.apple.coreservices.appleid.passwordcheck.plist -同上
> com.apple.coreservices.lsactivity.plist -IOS8新功能，ls激活，不知道什么东东，不建议删除
> 
> com.apple.coresymbolicationd.plist -未知，删除暂无影响
> 
> com.apple.CrashHousekeeping.plist -以下crash直接删除
> 
> com.apple.crashreportcopymobile.plist
> 
> com.apple.crash_mover.plist
> 
> <font color=red>com.apple.cvmsCompAgent_armv7.plist -CPU相关，不可删除</font>
> 
> <font color=red>com.apple.cvmsServ.plist -同上</font>
> 
> com.apple.dataaccess.dataaccessd.plist -删除后不能通Exchange或Google来同步，同时在设置->邮件、通讯录、日历里添加的天气、农历等将无法使用，我从来不用，直接删除了
> 
> com.apple.device-o-matic.plist -设备连接，删除暂无影响
> 
> com.apple.diagnosticd.plist -著名的诊断，直接删除
> 
> com.apple.discoveryd.plist -IOS8新功能，删除后将无法上网，亲测
> 
> com.apple.discoveryd_helper.plist -帮助，可以删除，暂无影响
> 
> com.apple.distnoted.xpc.daemon.plist -删除后新软件需重启才显示，不建议删除
> 
> com.apple.DMHelper.plist -开发者帮助，删除无影响
> 
> com.apple.DuetHeuristic-BM.plist -IOS8新功能，删除无影响
> 
> com.apple.DumpBasebandCrash.plist -以下dump直接删除
> 
> com.apple.DumpPanic.plist
> 
> com.apple.EscrowSecurityAlert.plist -安全警报，我删除暂无影响
> 
> <font color=red>com.apple.fairplayd.H1.plist -删除后软件无法使用，切不可删！</font>
> 
> com.apple.familycircled.plist -IOS8新功能，家庭圈子，可删
> 
> com.apple.familynotificationd.plist -同上
> 
> com.apple.FileCoordination.plist -文件相关，未测试，不建议删除
> 
> com.apple.FileProvider.plist -同上
> 
> com.apple.fseventsd.plist -这个必须删除，斯诺登怀疑这是苹果监听用户的后门
> 
> com.apple.ftp-proxy-embedded.plist -删除后插件不显示
> 
> com.apple.GameController.gamecontrollerd.plist -游戏相关
> 
> com.apple.gamed.plist -同上
> 
> com.apple.geod.plist -高德地图
> 
> com.apple.GSSCred.plist -IOS8新功能，貌似信用卡，我删除暂无影响
> 
> com.apple.healthd.plist -IOS8健康应用
> 
> com.apple.homed.plist -IOS8新功能，未知，我删除暂无影响
> 
> <font color=red>com.apple.hpfd.mobile.plist -电话功能，不可删</font>
> 
> com.apple.iad.limitadtrackingd.plist -未知，删除无影响
> 
> com.apple.iap2d.plist -以下为配件功能，不用可删除无影响
> 
> com.apple.iapauthd.plist
> 
> com.apple.iapd.plist
> 
> com.apple.iaptransportd.plist
> 
> com.apple.icloud.findmydeviced.plist -云服务发现我的iPhone，不用可删
> 
> com.apple.icloud.fmfd.plist -同上
> 
> com.apple.identityservicesd.plist -身份验证，不建议删除
> 
> com.apple.idscredentialsagent.plist -IOS8新功能，貌似什么ids证书
> 
> com.apple.idsremoteurlconnectionagent.plist -IOS8新功能，和imessage相关，删除后imessage连接非常慢
> 
> com.apple.imagent.plist -以下im开头的和imessage相关
> 
> com.apple.imautomatichistorydeletionagent.plist -自动历史删除记录？直接删除无影响
> 
> com.apple.imavagent.plist
> 
> com.apple.IMLoggingAgent.plist -log日志服务，直接删除
> 
> com.apple.ind.plist -未知，我删除暂无影响
> 
> com.apple.itunescloudd.plist -删除后APP里面看不到已购买项目
> 
> com.apple.itunesstored.plist -删除后不可用手机APP商店
> 
> <font color=red>com.apple.jetsamproperties.N94.plist -管理进程的内存占用分配与优先等级的进程</font>
> 
> com.apple.languageassetd.plist -可能和siri语音相关
> 
> com.apple.librariand.plist -据说和天气有关，但是我删除了一切正常
> 
> <font color=red>com.apple.locationd.plist -定位服务</font>
> 
> <font color=red>com.apple.lsd.plist -缓存用的，删除后非常卡</font>
> 
> com.apple.lskdd.plist -未知，我删除暂无影响
> 
> com.apple.lskdmsed.plist -同上
> 
> com.apple.managedconfiguration.mdmd.plist -移动设备管理，我删除暂无影响
> 
> <font color=red>com.apple.managedconfiguration.profiled.plist -不可删除，系统设置功能将不可用</font>
> 
> com.apple.managedconfiguration.teslad.plist -和特斯拉匹配？屌丝可以删除
> 
> com.apple.Maps.geocorrectiond.plist -高德地图
> 
> com.apple.Maps.pushdaemon.plist -功德地图推送，我删除暂无影响
> 
> com.apple.mDNSResponder.plist -删除后无法上网
> 
> com.apple.mDNSResponderHelper.plist -协助开启facetime和imessage
> 
> com.apple.mdt.plist -未知，我删除暂无影响
> 
> com.apple.mediaartworkd.plist -未知，我删除暂无影响
> 
> <font color=red>com.apple.medialibraryd.plist -删除后点击“关于本机”会闪退，有时还进不了桌面</font>
> 
> com.apple.mediaremoted.plist -未知，我删除暂无影响
> 
> <font color=red>com.apple.mediaserverd.plist -切不可删，删除后进不了桌面，也连不上电脑</font>
> 
> com.apple.mediastream.mstreamd.plist -媒体流，我删除暂无影响
> 
> com.apple.midiserver-ios.plist -我删除暂无影响
> 
> com.apple.misagent.plist - IOS8新功能，我删除暂无影响
> 
> com.apple.mobile.assertion_agent.plist -未知，我删除暂无影响
> 
> com.apple.mobile.cache_delete_app_container_caches.plist 以下为IOS8新功能
> 
> com.apple.mobile.cache_delete_daily.plist
> 
> com.apple.mobile.cache_delete_geo_tile_loader.plist
> 
> com.apple.mobile.cache_delete_itunes_store.plist
> 
> com.apple.mobile.cache_delete_music.plist
> 
> com.apple.mobile.fud.plist -未知，我删除暂无影响
> 
> com.apple.mobile.insecure_notification_proxy.plist -不安全的通知**？？我删除暂无影响
> 
> <font color=red>com.apple.mobile.installd.plist -删除后无法安装越狱程序</font>
> 
> <font color=red>com.apple.mobile.keybagd.plist -核心进程，删除后白苹果，连SSH都无法使用</font>
> 
> <font color=red>com.apple.mobile.lockbot.plist -核心进程，删除后白苹果，连SSH都无法使用</font>
> 
> <font color=red>com.apple.mobile.lockdown.plist -核心进程，删除后白苹果，连SSH都无法使用</font>
> 
> <font color=red>com.apple.mobile.notification_proxy.plist -通知功能</font>
> 
> com.apple.mobile.obliteration.plist -必须删除！禁用此服务设置里的抹掉所有内容将不可用。防止手贱点到造成白苹果
> 
> com.apple.mobile.softwareupdated.plist -固件升级用的，必须删
> 
> com.apple.mobile.storage_mounter.plist -该进程是苹果在未来设备及固件中开启的新功能，将允许你使用你的iPhone保持在“磁盘模式”。也就是相当于一块移动硬盘来使用，不过，在目前的固件中暂时不执行任何操作，因此可以安全地删除这一并未投入使用，且未来也未必会投入使用的“功能”。删吧
> 
> <font color=red>com.apple.mobileactivationd-iphoneos.plist -删除后将无法激活手机</font>
> 
> com.apple.mobileassetd.plist - “hey siri”功能
> 
> com.apple.mobilecheckpoint.checkpointd.plist -未知，我删除暂无影响
> 
> <font color=red>com.apple.MobileFileIntegrity.plist - 文件权限删除后第三方程序将无法运行 </font>
> 
> com.apple.mobilegestalt.xpc.plist -关于本机名称的功能，删除后不显示本机名
> 
> com.apple.MobileInternetSharing.plist -个人热点，不用可删
> 
> com.apple.mobilestoredemod.plist -未知，我删除暂无影响
> 
> <font color=red>com.apple.mobile_installation_proxy.plist -第三方软件安装相关启动项</font>
> 
> <font color=red>com.apple.mtmergeprops.plist -核心进程，触屏操作</font>
> 
> com.apple.nand_task_scheduler.plist -未知，我删除了暂无影响
> 
> com.apple.neagent-ios.plist -ne服务，不知道什么东西，我删除暂无影响
> 
> com.apple.nehelper.plist -帮助删除无影响
> 
> com.apple.nesessionmanager.plist -ne会话管理，不知道什么东西，我删除暂无影响
> 
> com.apple.networkd.plist -网络相关进程,删除后APP里面下不了东西
> 
> com.apple.networkd_privileged.plist - 特殊网络？我删除了暂无影响
> 
> com.apple.NetworkLinkConditioner.plist -链接？我删除了暂无影响
> 
> com.apple.nfsconf.plist -网络文件系统的配置文件进程启动项
> 
> <font color=red>com.apple.notifyd.plist -核心进程，通知相关，springboard 必备</font>
> 
> com.apple.nsurlsessiond.plist -亲测，删除后不能在APP里面下载软件
> 
> com.apple.nsurlstoraged.plist -亲测，删除后不能在APP里面下载软件
> 
> com.apple.OTACrashCopier.plist -以下OTA可以删除，越狱就不用OTA升级了
> 
> com.apple.OTAPKIAssetTool.plist
> 
> com.apple.OTATaskingAgent.plist
> 
> com.apple.passd.plist -passbook，不用可删
> 
> com.apple.pfd.plist -未知，我删除了暂无影响
> 
> <font color=red>com.apple.pipelined.plist -删除后各种耗电，不稳定</font>
> 
> com.apple.pluginkit.pkd.plist -IOS8新功能，就是通知中心里面的编辑功能，还有和第三方输入法有关
> 
> com.apple.pluginkit.pkreporter.plist -给上面的未知程序report用的，我直接删除，无影响
> 
> com.apple.powerd.plist -节能控制，删除后耗电
> 
> com.apple.powerlogd.plist -日志文件，直接删除
> 
> com.apple.prdaily.plist 打印日志，直接删除
> 
> com.apple.preboardservice.plist -IOS8新功能，预先加载桌面服务？但是我删除了没有任何影响
> 
> com.apple.printd.plist -打印功能，不用可以删除
> 
> com.apple.PurpleReverseProxy.plist IOS8新功能，我删除了暂无影响
> 
> com.apple.PurpleReverseProxy.ramdisk.plist 同上
> 
> com.apple.racoon.plist V*N用的
> 
> com.apple.recentsd.plist -未知，但我删除无影响
> 
> com.apple.ReportCrash.DirectoryService.plist 以下crash直接删除
> 
> com.apple.ReportCrash.Jetsam.plist
> 
> com.apple.ReportCrash.plist
> 
> com.apple.ReportCrash.SafetyNet.plist
> 
> com.apple.ReportCrash.SimulateCrash.plist
> 
> com.apple.ReportCrash.StackShot.plist
> 
> com.apple.reversetemplated.plist 未知，但我删除无影响
> 
> com.apple.revisiond.plist 未知，但我删除无影响
> 
> com.apple.rolld.plist 未知，但我删除无影响
> 
> com.apple.routined.plist 自带程序进程启动项，删除后定位-系统服务将不可用
> 
> com.apple.rtcreportingd.plist 未知，但我删除无影响
> 
> com.apple.safarifetcherd.plist 浏览器的什么，删除暂无影响
> 
> <font color=red>com.apple.sandboxd.plist -核心进程，删除后白苹果，连SSH都无法使用</font>
> 
> com.apple.sbd.plist 未知，但我删除无影响
> 
> com.apple.SCHelper-embedded.plist 系统设置相关，删除会导致黑屏后闹钟及日历提醒异常
> 
> com.apple.scrod.plist -未知，但我删除无影响
> 
> com.apple.search.appindexer.plist -搜索
> 
> com.apple.searchd.plist -搜索
> 
> com.apple.security.CircleJoinRequested.plist 以下为安全相关进程，不建议删除,但是我删除了也没什么影响
> 
> com.apple.security.cloudkeychainproxy.plist
> 
> com.apple.security.swcagent.plist
> 
> <font color=red>com.apple.securityd.plist -删除立马白苹果</font>
> 
> com.apple.softwarebehaviorservicesd.plist 以下为OTA升级服务
> 
> com.apple.softwareupdateservicesd.plist
> 
> com.apple.splashboardd.plist -未知，删除没任何影响
> 
> <font color=red>com.apple.SpringBoard.plist 核心进程，springboard 必备</font>
> 
> com.apple.storebookkeeperd.plist 书店进程守护启动项
> 
> com.apple.streaming_zip_conduit.plist 未知，但我删除无影响
> 
> com.apple.suggestd.plist 未知，但我删除无影响
> 
> com.apple.swcd.plist 未知，但我删除无影响
> 
> com.apple.syncdefaultsd.plist 默认同步，但我删除无影响
> 
> com.apple.syslogd.plist 以下为日志，直接删除
> 
> com.apple.syslog_relay.plist
> 
> <font color=red>com.apple.tccd.plist 核心进程，springboard 必备</font>
> 
> com.apple.telephonyutilities.callservicesd.plist 貌似电话服务，不建议删除
> 
> com.apple.TextInput.kbd.plist 打字进程启动项，除非你不打字
> 
> com.apple.timed.plist 时间相关
> 
> com.apple.timezoneupdates.tzd.plist 同上
> 
> com.apple.tipsd.plist 未知，但我删除无影响
> 
> com.apple.touchsetupd.plist 与设置apple TV相关，删除吧
> 
> com.apple.tzlinkd.plist 链接，删除吧，无影响
> 
> com.apple.ubd.plist 未知，但我删除无影响
> 
> com.apple.UIKit.pasteboardd.plist 复制粘贴功能
> 
> com.apple.usb.networking.addNetworkInterface.plist 可能是把iPhone当无线网卡的功能
> 
> <font color=red>com.apple.usbptpd.plist -核心进程，删除后白苹果，连SSH都无法使用</font>
> 
> <font color=red>com.apple.UserEventAgent-System.plist  如果删除，会有出现高温警告，无法进系统</font>
> 
> com.apple.voiced.plist - 语音相关，不用可以删
> 
> <font color=red>com.apple.voicemail.vmd.plist -切不可删，删除后进不了桌面，但是可以连电脑</font>
> 
> com.apple.voicememod.plist 语音相关，不用可以删
> 
> com.apple.VoiceOverTouch.plist 语音相关，不用可以删
> 
> com.apple.vsassetd.plist -未知，删除暂无影响
> 
> com.apple.WebBookmarks.webbookmarksd.plist 书签，不用删除吧
> 
> com.apple.webinspectord.plist 网页检查，但是我删了暂无影响
> 
> com.apple.wifi.hostapd.plist 以下和wifi相关
> 
> com.apple.wifi.wapic.plist
> 
> com.apple.wifid.plist
> 
> com.apple.wifiFirmwareLoader.plist
> 
> com.apple.wirelessproxd.plist

