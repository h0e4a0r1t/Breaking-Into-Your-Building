# Breaking-Into-Your-Building

## 一 、被动侦查
### 1. OSINT
*Google 街景地图
例如：使用街景地图查看目标建筑一楼各入口使用的安保设施
*社交媒体（工牌、用户名等敏感信息）
用户名收集（Github、百度贴吧等）
电子邮件搜索
域名（Google Dork、WHOIS、子域名收集）
无线网络信息
网络摄像头（Google Dork 或通过漏洞）（可获取建筑内部布局、员工个人习惯或看到员工工牌）
    例如： 可通过网络摄像头了解建筑布局，或者可以看到一些员工或者安保人员的个人习惯，也有可能会拍到员工的工牌，方便我们对员工工牌进行克隆模仿
文档和元数据 （Google Dork、EXIFTOOL等）（可通过文档的元数据获取到员工用户名）
    例如： 从网上找到该公司的pdf，通过元数据可提取出文档作者的用户名或邮箱
历史泄漏数据 
    例如： 如果密码是最喜欢的宠物的名字或者最喜欢的运动队的名字，可以在社会工程学中寻找话题及钓鱼利用
对钥匙（工牌）进行拍照，之后通过照片进行钥匙（工牌）克隆，仔细观察工牌的布局、挂绳及公司要求的着装规范
    例如：1. 可以实地拍摄（员工会在身上挂着钥匙/工牌，或者桌上放着）；2. 从社交媒体照片中获取；3. 从该公司的员工合照中可获取到工牌的样子；

### 2. Google Dork Example（更多详情请移步谷歌搜索数据库）
**寻找简历**
INURL:RESUMES "BRUSE WAYNE"  /  INTEXT:RESUMES "BRUSE WAYNE"
**用户名**
USERNAME *.com
**Github**
site:http://github.com/orgs/*/people
**文档**
site:<domain> filetype:pdf
文档包含邮箱:  filetype:pdf <domain> "email"
filetype: "xls | xlsx | doc | docx | csv | txt | pdf | log | sql" site:gov
**招聘信息（各大招聘网站）**
site: zhipin.com "Job Title" "位置"
site: zhipin.com "工程师" "上海"
site:zhipin.com "人名"   (通过人名来查找目标的一些特征)
**云端服务器**
site:"cloud.com" filetype:xls
**数据库**
ext:sql intext:"-- PHPMYADMIN SQL DUMP"
**包含密码的文件**
"USERNAME" "PASSWORD" ext:log
"'USERNAME' =>" + "'PASSWORD' =>" ext:log
intitle:"database.php" inurl:"database.php" intext:"db_password"
ext:txt intext:@targetemail.com intext:password
ext:xls intext:@targetemail.com intext:password
**网络摄像头**
inurl:"view.shtml" "network camera"
inurl:"multicameraframe?mode=motion"
allintitle: AXIS 2.10  OR 2.12  OR 2.30 OR 2.31  OR 2.32  OR 2.33 OR 2.34 OR 2.42 OR 2.40 OR 2.43  "network camera"
inurl:control/camerainfo
二 、主动侦查
1. 无人机入侵
在无人机上安放 "WI-FI 菠萝派" 进行无线网攻击
利用无人机拍摄难以拍摄的地方（例如通过大楼外窗拍摄室内桌子上的工牌或敏感文件）
切记遵守无人机法！！！
    例如：下班后，在目标建筑附近操控无人机，在晚上或者当保洁员将灯打开时，可以利用无人机高清晰度的摄像头窃取信息；或是一些员工会将敏感文件或信息留在桌子上，也可以通过无人机进行窃取

2. 拍摄工具
带有针孔摄像头的钢笔

带有针孔摄像头的打火机

不太建议使用带有摄像头的眼镜，较容易被发现

一双训练有素的眼睛（能够一眼发现需要的数据）
完美的伪装（外壳）
巧妙的隐藏
三 、融入环境
1. 需要考虑的点
目标的公司文化及着装要求（穿什么衣服）
掩饰身份（扮演什么身份）
与目标之间的距离
需要的装备（NFC卡克隆器）
    例如目标建筑正在施工，可以穿成建筑工人混入目标 / 或是在挤电梯的时候可以看到很多员工身上带着身份卡，可以在电梯内趁电梯拥挤或他人不注意进行NFC卡克隆，而不必去刻意的撞某人
四 、不需要钥匙的进入方式
1. 开锁工具（套装）
Mace Lockpicks

Door / Padlock Shims
10pcs Klom Padlock Shim Picks Set Locksmith Tool Lock Accessories Gadgets  Set | eBay
hall pass shove knife
CG's Physical Security Tools
RFID LF/HF Detector Card
Cheap Rfid Hf/lf Frequency Proximity Sensor Smart Rfid Wiegand Card Reader  Access Control - Buy Rfid Id/ic Card Reader Access Control,Smart Rfid Card  Reader 125khz,Cheap Rfid Card Reader 13.56mhz Product on Alibaba.com
Latch Slipping Shim

Handcuff Shims
Handcuff Shims
Quick Stick
SKLZ Pujols Quick Stick Lightweight Training Bat | HittingWorld.com
Doorking Master
Doorking Key Newer - Sockets - Amazon.com
Linear 222343
222343 - Linear
CH751
CH751 Replacement Switch Key
C415A
C415A_keys
Jigglers
Auto Jiggler Keys
Shrum Tool(Traveler's Hook)
Covert Entry Multi-tool Build – We Hack People – Covert Entry
Peterson Mini Knife Tool(Decoder)
Single Peterson Mini Knife Tool - ThinkPeterson.com
Peterson Knife Tool
Peterson Adams rite trip wire
Adams Rite DL Trip Wire - ThinkPeterson.com
Peterson america padlock bypass
American Padlock Bypass Tool - ThinkPeterson.com
2. 推荐工具

3. 推荐开门工具
1. 使用塑料片卡门
这里我就不做演示了，我在实际演示中发现是可以的；而且制作方便，找一块稍微硬一点的塑料片就可以轻松实现
具体原理地址：https://swiftsilentdeadly.com/how-to-shim-a-door-and-protect-yours/
具体视频地址：https://youtu.be/1Bj8JKN2pQQ
我在网上还看到另外一种方法，就是将卡片剪成这个样子，也是可以的

或者
2. 使用shove knife开门
原理同上

使用大号的 shove knife，来绕过在锁前加了一块挡板来防止塑料片或者普通的shove knike的场景

3. 使用衣架临时改装

4. 门下工具
使用衣架临时改装或使用该工具，可从底部伸入套在内侧门把手上实现开门

从门下伸入

使其套在门把手上，一拉门就打开了

像是圆形把手可以在绳子上绑上运动胶带，通过胶带的强粘性旋转门把手

5. Thumb-Turner Tool
拇指旋转锁的J工具
主要用于解锁在门内通过旋钮反锁的情况


6. Double Door Tool
Sparrows D.D.T (Double Door Tool) - Bypass Tools, Redteam Tools, Sparrows  Lock Picks - KSEC Labs
主要用于这样的双开门

或是

使用时从门缝塞入，旋转按压即可开门

或

7. 基于运动和温度的传感器

通过使用压缩空气从门的下方喷出来绕过传感器；

或在磁吸处趁不注意伸手贴一些异物，也可减少磁力

需要考虑的事情
使用回形针很明显
太过于减少门与锁之间的磁力，这会在其他人开门时容易引起怀疑
更好的选择
颜色几乎相同的隔绝物
更好的伪装
减少门与锁之间的磁力到刚好可以用力拉开

或者通过绑在铁丝上的暖手宝贴近传感器来绕过传感器

之前在客户那里也遇到过外面需要刷卡，内部的门上是侦测物体的传感器，后来通过门缝扔进去一张卡片就开了

4. 谨记
紧跟别人进入 / 利用别人进入 = 自由进入
5. 如何获取密码
用可擦除的荧光笔或紫外线粉快速地涂在按键上
当有人输入他们的密码时和他站在一起
用紫外线照射按键，看看是哪个按钮被按下了

6. 万能钥匙和相同型号的钥匙
普通文件柜钥匙
公共设施控制箱钥匙
通用门禁控制箱钥匙
Y11 Gas Pump key
Amazon.com : Gas Pump Keys TPX83 Replacement Lock Keys ESP Brand Pre-Cut to  Key Code TPX83 with 1" Key Ring : Office Products
CH751 
1284X Crown Vic Key

EK222,333,2233x EMKA 工业钥匙

针对国内很多通用钥匙网上也有卖的


7. 利用货梯
通常在人员流动较少的地方
通常无需工牌或刷卡即可完全进入所有楼层
8. 挂锁
自己训练时，刚开始可以买那种透明的挂锁进行训练，之后就可以使用一些常见通用型号的挂锁

这里可以图片演示下如何用 Padlock Shims 进行挂锁的bypass
将 Padlock Shims 套在钩环和锁身之间，并嵌入；为了使Padlock Shims起作用，钩环和挂锁主体上的孔之间必须有足够的间隙，以使shim能够插入;而且要选择适合钩环直径的shim 

插入后，使其绕钩环旋转，以使shim的舌头从侧面接近闩锁

一旦垫片旋转到足以松开锁定机构的位置，就可以拉出卸扣以打开锁

具体的还要自己去实践
9. 手铐
您什么时候会用到此操作？
        可能永远不会，这不是一个好主意
这是一个方便的技能吗？
        是的，犯罪分子都知道这项技能。此外，您永远不知道什么时候可能会派上用场
太敏感了，就不详细解说了；有兴趣的自己去实践吧，注意是练习！！！
分为单锁和双锁
如何挑选手铐05
单锁：
推荐工具曲别针或发卡
第一种：
将发卡在棘轮之间插入，尽量插入到底；之后将手铐再拧紧一点，以使发卡更深入一点，如下图就可以打开手铐了
如何通过匀场解锁没有钥匙的手铐


第二种：
先将发卡插入锁孔中将其弯折成“S”型
鲍比别针手铐
插入锁孔旋转发卡
下图为单/双锁的结构图
How to Pick Handcuffs - The Ultimate Guide
双锁手铐的锁紧机构
动图
How to Pick Handcuffs - The Ultimate Guide
我自己也在网上买了几个手铐，别问，问就是带情趣俩字的；没意思，一下子就开了，而且和真锁有很大的区别～

9. 工牌克隆
不用技术的克隆

工牌的克隆

分为两种：高频和低频

一些伪装



9. USB攻击
键盘记录器（记录所有按键）
BadUSB
Bash Bunny
橡皮鸭
WIFI橡皮鸭
WIFI HID Injector   
