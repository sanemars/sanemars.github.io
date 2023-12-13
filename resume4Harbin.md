# 联系方式

- 手机：13313678256

- Email：sanemars@163.com

- 微信号：sanemars

# 个人信息

- 张国庆/男/1988

- 本科/东北林业大学机械电子工程专业

- 相关工作年限：8年

- 工作年限：10年

- StackOverflow：[https://stackoverflow.com/users/story/5084911](https://stackoverflow.com/users/story/5084911)

- 期望职位：Android高级开发工程师

- 期望薪资：税前月薪12k

- 期望城市：哈尔滨

# 工作经历

## Keep 北京卡路里信息技术有限公司（ 2018年8月 ~ 2023年8月 ）

### 直播课

- 负责设计、开发、维护
- 为提高协同开发效率、提高直播业务可维护性，完成直播业务框架的两次升级。使用 View Intersects 实现无业务逻辑关联的蒙层互斥管理器；使用 LiveData 实现模块与模块间、模块与模块插件间、模块插件与模块插件无耦合通信管理器。并提供了模块无限扩展能力；使用 AsyncLayoutInflater 加载各个模块、插件布局减少模块集中初始化时页面的卡顿率
  - 模块化直播业务，提升协同开发效率
- 为提升开发效率 ，编写直播业务模版代码生成插件
- 从用户体验测优化直播间秒开 ，优化直播间相关仪表盘绘制（视图缓存，shader 复用，禁绘重叠区域），内存泄漏排查修复

### 课程引擎

- 为提高户投屏练课体验，完善、优化基于 DLNA 的训练进度与投屏播放进度同步逻辑，增加智慧投屏，镜像投屏能力
- 使用单独进程与 AIDL 在用户无感知的情况下 实现并完善 Keep DMC

### KeepLand

- 带领1人负责 Keepland 线下运动空间播放教学系统的设计、开发、维护，协助运维及空间智能化改造
- 为解决原日志模块造成的 CPU 占用过高、界面卡顿、OOM问题，重构日志模块，原逻辑：日志写入 SQLite -> 从 SQLite 读取数据到文件 -> 压缩文件 -> 上传；重构逻辑：写文件 -> 课间上传
- 为提高数课程据传输效率，重构课程详情数据结构，使课程详情数据大小变为原来大小的15%
- 为提高运维效率，利用 IPSec 建立 VPN 并在设备端集成 SHH 服务，实现远程运维。
- 为提高播放系统稳定性，完善系统架构。本地时钟模块、SSH 服务、日志服务、故障自动恢复模块、心跳服务、缓存模块、训练指令分发模块，并重构训练背景音乐逻辑，使播放系统稳定性从 91.50% 提高到 99.70% 并实现了自动化、傻瓜式的播放系统
- 解决[体感游戏](/archives/images/motionSensingame.gif)技术难点，实现100ms以内延迟视频传输 (3D景深摄像头与游戏服务器连接，负责骨骼、动作识别，Android 盒子负责展示结果)

### 播放系统安装管家

- 人工仅需操作3步，即可完成电视盒子的 root，播放系统的安装、设置等操作 (利用 AccessibilityService、Shell 脚本、Settings)

### 其他项目

- 主导设计 Keepland 空间使用 Keep 手环收集心率技术方案
- 主导设计播放系统运行分析工具，量化播放系统稳定性指标
- 主导设计多屏联动动效
- 为 Keepland 空间智能化提供基础支持 (集成 Alot 设备与监控)
- 认真仔细进行 code review，通过 code review 阶段避免数个 P0，P1 问题
- 结合自身体验，发现 Keep 镜像画面白边问题，并提出解决方案

## 魔利互通(北京)信息技术有限公司 （ 2015年3月 ~ 2018年6月 ）

### [爱盈利ORP](archives/iem)

### [今麦郎终端管理系统](/archives/images/jml_NFC_Tag.gif)

### 中粮肉食

- 带领 5 人团队负责 5 款 App 的开发、整体可维护性、稳定性及安全性
- 为降低 App 升级时产生的流量 (流量费用来自七牛，截至2018年3月节约流量1.4TB)，实现App的增量升级 (使用 bsdiff 计算APK文件二进制差异，并通过 Huffman 算法压缩生成的差异文件)。过程中遇到 signal 内联函数在 android-21 平台下被取消的问题，通过修改 targetSdkVersion 生成不同 so 库，针对相应平台加载不同版本的 so 库。并发现android-21 平台下生成的 so 库体积小，故通过 Flavors 生成适用于不同平台的 App (android-21平台下的 App 体积更小)
- 为方便开发人员快速定位、修复用户使用 App 过程中遇到的崩溃，引入应用崩溃收集系统（BugTags）。第一时间获取异常信息，并经过一段时间的持续收集使应用的崩溃率从 2% 降低到 0.1%
- 为减少因修复 App BUG 而升级的情况，引入热修复机制。先后调研了 Tinker (基于 multidex) 与 AndFix (基于native hook) 后者对系统资源占用很少，但因为 Android 系统所用虚拟机和指令集的问题导致兼容性较差，最后采用 Robust (插桩，兼顾性能和实时修复) 实现热修复。可在用户无感的情况下修复 BUG，提高了用户体验
- 因业务需要，App 必须支持离线操作，导致大量业务数据存储在 SQLite 中，考虑到安全性，需对数据进行加密。采用了 sqlcipher，因涉及到用户 App 上的历史数据(历史数据未加密)， 故实现了数据的自动切换 (未加密数据切换成加密数据)。并在使用 sqlcipher 的过程中发现 3.58 、3.59 版本，在 armebi 下 limit 语句的 [BUG](https://github.com/sqlcipher/android-database-sqlcipher/issues/374)
- 因长期迭代及快速开发，导致应用内，存在大量的 Cursor 泄漏，人工查找效率低下且容易遗漏，故在 Debug 版及 Beta 版 App 中集成 Cursor 泄漏监控器，发现 Cursor 泄漏后第一时间将泄漏位置日志上报到服务器，方便开发人员统一修复
- 为查找莫名原因造成的 App 异常，开发实时日志收集系统。用户开启后，开发人员可在后台实时查看用户端上传的日志，方便排查问题
- 为提高 App 防破解能力，实现 Native 层的 App 签名校验
- 因业务原因 App 需要多套皮肤且不同皮肤的 App 相互独立。考虑到应用中隐士意图的跳转、FileProvider authorities 的唯一及第三方 key 与包名的关联，利用 Jenkins、BuildType 及 AndroidManifest 占位符实现多皮肤独立 App 的生成
- 为便于更新、查看 API 文档，采用 GitBook 与 apidoc 制作在线文档并利用 Jenkins 实时发布
- 为节省测试资源，搭建 UI 自动化测试平台 (使用 Espresso 编写 UI 测试用例，Spoon 管理、生成友好的测试结果并结合 Jenkins 持续集成)

### 其他项目

- 为测试人员开发，压测推送服务器小工具 (主要测试最大连接数)
- 为行政人事开发，工作周报模版生成工具。使制作工作周报的时间缩短为原来的 1/3
- 为处理照片上传事故，开发照片辅助上传工具。涉及 zip 包解压、数据库解密、业务数据分析、修复和照片文件上传

## 学习Android程序开发 （ 2014年9月 ~ 2015年3月 ）

### [微身边](http://www.circlefil.com/)

- 基于 Openfire、Asmack 框架的聊天、社交软件。实现了用户注册、登录、添加好友、得到好友分类信息、私聊、群聊，支持文字、表情、图片、语音、地图的发送，话题的发表及在地图上显示话题等功能
- 聊天内容通过 Native 进行加密，解密，通过 Wireshark 来获取网络数据包，查看加密效果
- 采用多个自定义 View 如 SlidingMenu，GifView，CircleImageView
- 采用异步联网框架 AsyncHttpClient,异步加载图片
- 采用单例，工厂，IOC，观察者等设计模式
- 实现服务器上的 Servlet，存放最新版本的 APK，客户端通过网络得获取最新版本，进行 App 版本管理
- 发送图片时，用 Base64 将图片转成字符串，收到后再用单线程轮询机制进行 Base64 解码，并存入SD card。发语音时用 MediaRecorder 录音，存到 SD card 上再用 MediaPlayer 进行播放
- 通过此项目，提高了编写 Android 应用软件的综合能理。了解了Android NDK 的使用，强化了使用第三方框架做二次开发的能力

## 哈尔滨分众传媒有限公司 （ 2014年3月 ~ 2014年8月 ）

### 安装维修员

- 通过学习并结合实践，快速掌握工作相关技能，高效完成工作任务

## 开淘宝网店 （ 2013年3月 ~ 2014年2月 ）

### 主营虚拟物品

- 增强了Photoshop 处理图片的能力，学会了 Illustrator 的使用

## 哈尔滨空调股份有限公司（ 2012年9月 ~ 2013年2月 ）

### 产品检查员

- 按照行业标准，严格执行企业规章制度要求，严把质量检验关，做到产品合格率100%
- 归档文件、材料明细清晰

# 演讲和讲义

- 2018年1月：[竞品分析之安全性](https://sanemars.github.io/archives/competitiveAnalysis.html#/)
- 2019年1月：[CoAP 简介与使用](https://yanshuo.io/assets/player/?deck=5c231e434773f7173688424e#/)

# 技能清单

以下均为我熟练使用的技能

- 移动开发：Android/Java/Kotlin/Jetpack/JNI/Groovy
- 移动端框架：okhttp/retrofit/glide/butterknife/MPAndroidChart/ANR-WatchDog/sqlcipher/CoAP
- 数据库相关：SQLite/MySQL
- 版本管理、文档和自动化部署工具：Svn/Git/GitBook/Jenkins/Phabricator
- 自动化测试：Espresso/Spoon
- 调试工具：AndroidStudio/fiddler/apktool/Proxyman

# 致谢

感谢您花时间阅读我的简历，期待能有机会和您共事。
