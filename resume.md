# 联系方式

- 手机：18010456857

- Email：tsanemars@gmail.com

- 微信号：sanemars

# 个人信息

- 张国庆/男/1988

- 本科/东北林业大学机械电子工程专业

- 相关工作年限：3年

- 工作年限：6年

- StackOverflow：[https://stackoverflow.com/users/story/5084911](https://stackoverflow.com/users/story/5084911)

- 期望职位：Android高级开发工程师

- 期望薪资：税前月薪26k

- 期望城市：北京

  

# 工作经历

  

## 魔利互通(北京)信息技术有限公司 （ 2015年3月 ~ 至今 ）

  

### 爱盈利ORP

### 今麦郎终端管理系统

### 中粮肉食
- 负责5款App整体可维护性、稳定性及安全性
- 为降低App升级时产生的流量(流量费用来自七牛，截至2018年3月节约流量1.4TB)，实现App的增量升级(使用bsdiff计算APK文件二进制差异，并通过Huffman算法压缩生成的差异文件)。过程中遇到 signal内联函数在android-21平台下被取消的问题，通过修改targetSdkVersion生成不同so库，针对相应平台加载不同版本的so库。并发现android-21平台下生成的so库体积小，故通过Flavors生成适用于不同平台的App(android-21平台下的App体积更小)
- 为方便开发人员快速定位、修复用户使用App过程中遇到的崩溃，引入应用崩溃收集系统（BugTags）。第一时间获取异常信息，并经过一段时间的持续收集使应用的崩溃率从2%降低到0.1%
- 为减少因修复App BUG而升级的情况，引入热修复机制。先后调研了Tinker(基于multidex)与AndFix(基于native hook)后者对系统资源占用很少，但因为Android系统所用虚拟机和指令集的问题导致兼容性较差，最后采用Robust(插桩，兼顾性能和实时修复)实现热修复。可在用户无感的情况下修复BUG，提高了用户体验 
- 因业务需要，App必须支持离线操作，导致大量业务数据存储在SQLite中，考虑到安全性，需对数据进行加密。采用了sqlcipher，因涉及到用户App上的历史数据(历史数据未加密)， 故实现了数据的自动切换(未加密数据切换成加密数据)。并在使用sqlcipher的过程中发现3.58 、3.59版本，在armebi下 limit语句的[BUG](https://github.com/sqlcipher/android-database-sqlcipher/issues/374)。
- 因长期迭代及暴力开发，导致应用内，存在大量的Cursor泄漏，人工查找效率低下且容易遗漏，故在Debug版及Beta版App中集成Cursor泄漏监控器，发现Cursor泄漏后第一时间将泄漏位置日志上报到服务器，方便开发人员统一修复
- 为查找莫名原因造成的App异常，开发实时日志收集系统。用户开启后，开发人员可在后台实时查看用户端上传的日志，方便排查问题
- 为提高App防破解能力，实现Native层的App签名校验
- 因业务原因App需要多套皮肤且不同皮肤的App相互独立。考虑到应用中隐士意图的跳转、FileProvider authorities的唯一及第三方key与包名的关联，利用Jenkins、BuildType及AndroidManifest占位符实现多皮肤独立App的生成
- 为便于更新、查看API文档，采用GitBook与apidoc制作在线文档并利用Jenkins实时发布
- 为节省测试资源，搭建UI自动化测试平台(使用Espresso编写UI测试用例，Spoon管理、生成友好的测试结果并结合Jenkins持续集成)

### 其他项目

- 为测试人员开发，测试推送服务器压力小工具(主要测试最大连接数 )
- 为行政人事开发，工作周报模版生成工具。使制作工作周报的时间缩短为原来的1/3
- 为处理照片上传事故，开发照片辅助上传工具。涉及zip包解压、数据库解密、业务数据分析、修复和照片文件上传
  

## 学习Android程序开发 （ 2014年9月 ~ 2015年3月 ）
### 微身边

- 基于Openfire、Asmack框架的聊天、社交软件。实现了用户注册、登录、添加好友、得到好友分类信息、私聊、群聊，支持文字、表情、图片、语音、地图的发送，话题的发表及在地图上显示话题等功能
- 聊天内容通过Native进行加密，解密，通过Wireshark来获取网络数据包，查看加密效果
- 采用多个自定义View如SlidingMenu，GifView，CircleImageView
- 采用异步联网框架AsyncHttpClient,异步加载图片
- 采用单例，工厂，IOC,观察者等设计模式
- 实现服务器上的Servlet，存放最新版本的APK，客户端通过网络得获取最新版本，进行App版本管理
- 发送图片时，用Base64将图片转成字符串，收到后再用单线程轮询机制进行Base64解码，并存入SD card。发语音时用MediaRecorder录音，存到SD card上再用MediaPlayer进行播放
- 通过此项目，提高了编写Android应用软件的综合能理。了解了Android NDK的使用，强化了使用第三方框架做二次开发的能力

## 哈尔滨分众传媒有限公司 （ 2014年3月 ~ 2014年8月 ）

###  安装维修员
 
 - 学会了视频播放器高清板的维修、改造

## 开淘宝网店 （ 2013年3月 ~ 2014年2月 ）

### 主营虚拟物品

- 增强了Photoshop 拼图的能力，学会了Illustrator的使用

## 哈尔滨空调股份有限公司（ 2012年9月 ~ 2013年2月 ）

### 产品检查员

- 提高了文件归档能力，增强了人际沟通能力

# 演讲和讲义

- 2018年1月：[竞品分析之安全性](https://sanemars.github.io/archives/competitiveAnalysis.html#/)

# 技能清单

以下均为我熟练使用的技能

- 移动开发：Android/Java/JNI/Groovy

- 移动端框架：okhttp/retrofit/glide/butterknife/MPAndroidChart/ANR-WatchDog/sqlcipher
- 数据库相关：SQLite/MySQL
- 版本管理、文档和自动化部署工具：Svn/Git/GitBook/Jenkins
- 自动化测试：Espresso/Spoon
- 调试工具：AndroidStudio/Fidder/apktool

# 致谢

感谢您花时间阅读我的简历，期待能有机会和您共事。
