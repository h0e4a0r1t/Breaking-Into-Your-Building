# Breaking-Into-Your-Building

## 一 、被动侦查

### OSINT

- Google 街景地图

   例如：使用街景地图查看目标建筑一楼各入口使用的安保设施

- 社交媒体（工牌、用户名等敏感信息）

- 用户名收集（Github、百度贴吧等）

- 电子邮件搜索

- 域名（Google Dork、WHOIS、子域名收集）

- 无线网络信息

- 网络摄像头（Google Dork 或通过漏洞）（可获取建筑内部布局、员工个人习惯或看到员工工牌）

  例如： 可通过网络摄像头了解建筑布局，或者可以看到一些员工或者安保人员的个人习惯，也有可能会拍到员工的工牌，方便我们对员工工牌进行克隆模仿

- 文档和元数据 （Google Dork、EXIFTOOL等）（可通过文档的元数据获取到员工用户名）

   例如： 从网上找到该公司的pdf，通过元数据可提取出文档作者的用户名或邮箱

- 历史泄漏数据 

  例如： 如果密码是最喜欢的宠物的名字或者最喜欢的运动队的名字，可以在社会工程学中寻找话题及钓鱼利用

- 对钥匙（工牌）进行拍照，之后通过照片进行钥匙（工牌）克隆，仔细观察工牌的布局、挂绳及公司要求的着装规范

   例如：1. 可以实地拍摄（员工会在身上挂着钥匙/工牌，或者桌上放着）；2. 从社交媒体照片中获取；3. 从该公司的员工合照中可获取到工牌的样子；

### Google Dork Example（更多详情请移步谷歌搜索数据库）

**寻找简历**

```
INURL:RESUMES "BRUSE WAYNE"  /  INTEXT:RESUMES "BRUSE WAYNE"
```

**用户名**

```
USERNAME *.com
```

**Github**

```
site:http://github.com/orgs/*/people
```

**文档**

```
site:<domain> filetype:pdf
文档包含邮箱:  filetype:pdf <domain> "email"
filetype: "xls | xlsx | doc | docx | csv | txt | pdf | log | sql" site:gov
```

**招聘信息（各大招聘网站）**

```
site: zhipin.com "Job Title" "位置"
site: zhipin.com "工程师" "上海"
site:zhipin.com "人名"   (通过人名来查找目标的一些特征)
```

**云端服务器**

```
site:"cloud.com" filetype:xls
```

**数据库**

```
ext:sql intext:"-- PHPMYADMIN SQL DUMP"
```

**包含密码的文件**

```
"USERNAME" "PASSWORD" ext:log
"'USERNAME' =>" + "'PASSWORD' =>" ext:log
intitle:"database.php" inurl:"database.php" intext:"db_password"
ext:txt intext:@targetemail.com intext:password
ext:xls intext:@targetemail.com intext:password
```

**网络摄像头**

```
inurl:"view.shtml" "network camera"
inurl:"multicameraframe?mode=motion"
allintitle: AXIS 2.10  OR 2.12  OR 2.30 OR 2.31  OR 2.32  OR 2.33 OR 2.34 OR 2.42 OR 2.40 OR 2.43  "network camera"
inurl:control/camerainfo
```

## 二 、主动侦查

1. ### 无人机入侵

- 在无人机上安放 "WI-FI 菠萝派" 进行无线网攻击

- 利用无人机拍摄难以拍摄的地方（例如通过大楼外窗拍摄室内桌子上的工牌或敏感文件）

- 切记遵守无人机法！！！

   例如：下班后，在目标建筑附近操控无人机，在晚上或者当保洁员将灯打开时，可以利用无人机高清晰度的摄像头窃取信息；或是一些员工会将敏感文件或信息留在桌子上，也可以通过无人机进行窃取

  

   ![image](https://user-images.githubusercontent.com/48357278/127758858-76667394-8b04-4b8b-aba8-42f68fa1eb61.png)


2. ### 拍摄工具

- 带有针孔摄像头的钢笔

  ![image](https://user-images.githubusercontent.com/48357278/127758869-d3d00c56-ba95-4280-8264-607bd2d002c5.png)


- 带有针孔摄像头的打火机

  ![image](https://user-images.githubusercontent.com/48357278/127758873-d6cc10a3-b372-48eb-8bb2-7a58ecf5524c.png)


- 不太建议使用带有摄像头的眼镜，较容易被发现

  ![image](https://user-images.githubusercontent.com/48357278/127758875-83b81e6d-e1eb-49a7-a280-2a8bdeaf724e.png)


- 一双训练有素的眼睛（能够一眼发现需要的数据）
- 完美的伪装（外壳)
- 巧妙的隐藏

## 三 、融入环境

1. ### 需要考虑的点

- 目标的公司文化及着装要求（穿什么衣服）

- 掩饰身份（扮演什么身份）

- 与目标之间的距离

- 需要的装备（NFC卡克隆器）

   例如: 目标建筑正在施工，可以穿成建筑工人混入目标 / 或是在挤电梯的时候可以看到很多员工身上带着身份卡，可以在电梯内趁电梯拥挤或他人不注意进行NFC卡克隆，而不必去刻意的撞某人

## 四 、不需要钥匙的进入方式

1. ### 开锁工具（套装）

- Mace Lockpicks

  ![image](https://user-images.githubusercontent.com/48357278/127758879-af8782e2-a257-4371-8c6d-1a7049a1dc27.png)


- Door / Padlock Shims

 ![image](https://user-images.githubusercontent.com/48357278/127758884-1f4d0828-2fc1-4b4e-80e0-3bedf66429aa.png)


- hall pass shove knife

  ![image](https://user-images.githubusercontent.com/48357278/127758888-d16a42a4-c4f2-4f65-bfaa-fa337b1920ed.png)


- RFID LF/HF Detector Card

  ![image](https://user-images.githubusercontent.com/48357278/127758890-3eb4ad1b-d1e7-4269-b877-3769499106be.png)


- Latch Slipping Shim

  ![image](https://user-images.githubusercontent.com/48357278/127758896-7774f0e9-db4a-4764-87de-f78423043867.png)

- Handcuff Shims

  ![image](https://user-images.githubusercontent.com/48357278/127758912-f1701341-fa1e-492b-9ef4-3c9a20b2908b.png)

- Quick Stick

  ![image](https://user-images.githubusercontent.com/48357278/127758919-6c282e4f-148b-4ca9-a684-1563d63c458a.png)


- Doorking Master

  ![image](https://user-images.githubusercontent.com/48357278/127758934-221e3046-fee3-45e6-8d32-90cbe01d289b.png)

- Linear 222343

  ![image](https://user-images.githubusercontent.com/48357278/127758946-186e0502-0e7e-43a3-b76a-d4d9307db908.png)

- CH751

  ![image](https://user-images.githubusercontent.com/48357278/127758947-a188ff00-e847-47e9-a886-b0f7c3d99c69.png)

- C415A

  ![image](https://user-images.githubusercontent.com/48357278/127758953-c5cc8df9-cac2-45ff-8eb9-e42e1627e2e0.png)


- Jigglers

![image](https://user-images.githubusercontent.com/48357278/127758955-66a26259-839f-48a3-a993-e186caad9f2b.png)


- Shrum Tool(Traveler's Hook)

![image](https://user-images.githubusercontent.com/48357278/127758961-00ed7fd8-a7ce-470d-99cb-4588c3e8bdc3.png)


- Peterson Mini Knife Tool(Decoder)

  ![image](https://user-images.githubusercontent.com/48357278/127758964-3043f32f-acf2-43c6-8b27-a11894c0da95.png)

- Peterson Knife Tool

- Peterson Adams rite trip wire

 ![image](https://user-images.githubusercontent.com/48357278/127758968-ff6965ad-0cd4-42da-a834-10668c723a96.png)


- Peterson america padlock bypass

 ![image](https://user-images.githubusercontent.com/48357278/127758971-aa6bcc13-871c-4204-9a4c-600fb127fc46.png)


2. ### 推荐工具

  
 ![image](https://user-images.githubusercontent.com/48357278/127758976-8fa64fa0-43d2-4f67-b52c-1cf5b19098ee.png)


  

3. ### 推荐开门工具

   1. #### 使用塑料片卡门

   这里我就不做演示了，我在实际演示中发现是可以的；而且制作方便，找一块稍微硬一点的塑料片就可以轻松实现
   
   具体原理地址：https://swiftsilentdeadly.com/how-to-shim-a-door-and-protect-yours/
   具体视频地址：[https://youtu.be/1Bj8JKN2pQQ](https://youtu.be/1Bj8JKN2pQQ)
   
   我在网上还看到另外一种方法，就是将卡片剪成这个样子，也是可以的
   
   ![image](https://user-images.githubusercontent.com/48357278/127758981-272426b0-bc94-4b14-8ab1-89569d006a10.png)
   
   或者

   2. #### 使用shove knife开门

   原理同上

   ![image](https://user-images.githubusercontent.com/48357278/127758986-17f83df7-2a5b-4e28-b277-c66c524310ff.png)

   使用大号的 shove knife，来绕过在锁前加了一块挡板来防止塑料片或者普通的shove knike的场景

   ![image](https://user-images.githubusercontent.com/48357278/127758989-883bb050-0741-4f22-b876-037b0fb15750.png)


   3. #### 使用衣架临时改装

   4. #### 门下工具

   使用衣架临时改装或使用该工具，可从底部伸入套在内侧门把手上实现开门

   ![image](https://user-images.githubusercontent.com/48357278/127758993-05571e9a-811f-4325-8786-5baa4fff3646.png)


   从门下伸入

   ![image](https://user-images.githubusercontent.com/48357278/127758994-77182552-8a80-4766-aded-aaed597d1bea.png)


   使其套在门把手上，一拉门就打开了

   ![image](https://user-images.githubusercontent.com/48357278/127759001-b1779503-c052-407c-9aeb-824cc447ee39.png)


   像是圆形把手可以在绳子上绑上运动胶带，通过胶带的强粘性旋转门把手

   ![image](https://user-images.githubusercontent.com/48357278/127758997-994f5985-1c14-4953-90a8-3951e6ea56e6.png)

   5. #### Thumb-Turner Tool

      ![image](https://user-images.githubusercontent.com/48357278/127758998-f5fad4d7-77a5-439c-8cc7-a99ab2ad678f.png)
      
      主要用于解锁在门内通过旋钮反锁的情况

      ![image](https://user-images.githubusercontent.com/48357278/127759007-dbb1a4ec-457e-4c79-996c-fdeda1c66c77.png)

      ![image](https://user-images.githubusercontent.com/48357278/127759014-48063784-4918-48c6-b4e7-661d4e34cca2.png)

   6. #### Double Door Tool


      ![image](https://user-images.githubusercontent.com/48357278/127759008-a419984e-48bf-487d-b37d-bb3aed3708fc.png)

      主要用于这样的双开门

      ![image](https://user-images.githubusercontent.com/48357278/127759017-06607dba-8b65-4c10-a184-c54bf2d5c6f3.png)

      或是

      ![image](https://user-images.githubusercontent.com/48357278/127759021-623b4f4e-6f30-4720-9833-855eed68dd42.png)


      使用时从门缝塞入，旋转按压即可开门

      ![image](https://user-images.githubusercontent.com/48357278/127759025-3c5078a3-601f-407b-8874-554e86de072b.png)

      或

      ![image](https://user-images.githubusercontent.com/48357278/127759030-60caf0b0-f87f-4a3e-895a-bfe487cb0fb3.png)

   7. #### 基于运动和温度的传感器

      

      ![image](https://user-images.githubusercontent.com/48357278/127759032-9fd7c63f-2ffc-4388-b1d6-dc5fec2404f7.png)

      通过使用压缩空气从门的下方喷出来绕过传感器；

      ![image](https://user-images.githubusercontent.com/48357278/127759034-a2d19fb8-c921-4c90-93a5-af35cfafc655.png)


      或在磁吸处趁不注意伸手贴一些异物，也可减少磁力

      ![image](https://user-images.githubusercontent.com/48357278/127759035-ce783728-4e6b-4f97-9a48-b7eadafba4f1.png)


**需要考虑的事情**

- 使用回形针很明显
- 太过于减少门与锁之间的磁力，这会在其他人开门时容易引起怀疑

**更好的选择**

- 颜色几乎相同的隔绝物
- 更好的伪装
- 减少门与锁之间的磁力到刚好可以用力拉开

或者通过绑在铁丝上的暖手宝贴近传感器来绕过传感器

![image](https://user-images.githubusercontent.com/48357278/127759040-ad53792f-1cd6-4f66-803f-3a89f22884f0.png)

之前在客户那里也遇到过外面需要刷卡，内部的门上是侦测物体的传感器，后来通过门缝扔进去一张卡片就开了



4. ### 谨记

   - 紧跟别人进入 / 利用别人进入 = 自由进入

5. ### 如何获取密码

- 用可擦除的荧光笔或紫外线粉快速地涂在按键上
- 当有人输入他们的密码时和他站在一起
- 用紫外线照射按键，看看是哪个按钮被按下了

![image](https://user-images.githubusercontent.com/48357278/127759043-7d120b09-13bb-436f-9abe-6f8f4fd09151.png)

6. ### 万能钥匙和相同型号的钥匙

- 普通文件柜钥匙

- 公共设施控制箱钥匙

- 通用门禁控制箱钥匙

- Y11 Gas Pump key

  ![image](https://user-images.githubusercontent.com/48357278/127759047-dcbab105-70c4-47c5-bcc6-c4bfdc9a2096.png)


- CH751 

- 1284X Crown Vic Key

  ![image](https://user-images.githubusercontent.com/48357278/127759056-fb00b244-00fd-4d3e-8508-9e0ab7fac6de.png)

- EK222,333,2233x EMKA 工业钥匙

  ![image](https://user-images.githubusercontent.com/48357278/127759051-26c35960-f7e3-426e-b0d3-62266f5be903.png)


- 针对国内很多通用钥匙网上也有卖的

  ![image](https://user-images.githubusercontent.com/48357278/127759059-ccf4c7b5-53a3-44dd-87a1-c113ddb1925f.png)

  ![image](https://user-images.githubusercontent.com/48357278/127759063-2dcc4c0c-80e6-45e3-8621-4aa3789d9d5c.png)

### 7.利用货梯

- 通常在人员流动较少的地方
- 通常无需工牌或刷卡即可完全进入所有楼层

8. ### 挂锁

   自己训练时，刚开始可以买那种透明的挂锁进行训练，之后就可以使用一些常见通用型号的挂锁

   ![image](https://user-images.githubusercontent.com/48357278/127759066-fcd1f6fb-59fb-4b0c-b6b5-c8e53ea8d04e.png)

   这里可以图片演示下如何用 Padlock Shims 进行挂锁的bypass

   将 Padlock Shims 套在钩环和锁身之间，并嵌入；为了使Padlock Shims起作用，钩环和挂锁主体上的孔之间必须有足够的间隙，以使shim能够插入;而且要选择适合钩环直径的shim 

   ![image](https://user-images.githubusercontent.com/48357278/127759071-6969a88c-c94e-4987-b7e6-91016c8da2dc.png)


   插入后，使其绕钩环旋转，以使shim的舌头从侧面接近闩锁

   ![image](https://user-images.githubusercontent.com/48357278/127759074-32f292d9-b8b2-4b52-b3cc-4a166d635d37.png)

   一旦垫片旋转到足以松开锁定机构的位置，就可以拉出卸扣以打开锁

   ![image](https://user-images.githubusercontent.com/48357278/127759076-72160556-fb4f-4125-8b04-370c537e374e.png)

   具体的还要自己去实践

8. ### 手铐

- 您什么时候会用到此操作？
       可能永远不会，这不是一个好主意
- 这是一个方便的技能吗？
       是的，犯罪分子都知道这项技能。此外，您永远不知道什么时候可能会派上用场
- 太敏感了，就不详细解说了；有兴趣的自己去实践吧，注意是练习！！！

**分为单锁和双锁**

![image](https://user-images.githubusercontent.com/48357278/127759079-106c753c-390c-4f44-a363-f17ffc9af9fe.png)

**单锁：**

推荐工具曲别针或发卡

**第一种：**

将发卡在棘轮之间插入，尽量插入到底；之后将手铐再拧紧一点，以使发卡更深入一点，如下图就可以打开手铐了

![image](https://user-images.githubusercontent.com/48357278/127759082-52f6fe1a-f93d-4e75-9eee-0f2220b713b8.png)


![image](https://user-images.githubusercontent.com/48357278/127759094-7cc17e49-c7b1-4555-9a7d-f2a1fceffefd.png)

![image](https://user-images.githubusercontent.com/48357278/127759095-37bdb6e2-77bf-4cd2-943b-30728a40c646.png)

**第二种：**

先将发卡插入锁孔中将其弯折成"S"型

![image](https://user-images.githubusercontent.com/48357278/127759092-2de28b37-6c7b-4046-8fea-07cd68253fb4.png)


插入锁孔旋转发卡

下图为单/双锁的结构图

![image](https://user-images.githubusercontent.com/48357278/127759101-9fd8088b-b85e-499d-a196-eb13359f9e78.png)

![image](https://user-images.githubusercontent.com/48357278/127759107-f6b0ee3d-4a2e-42c2-b5f9-2fa1a1f707ee.png)


动图

![image](https://user-images.githubusercontent.com/48357278/127759102-5e7fd023-241f-4729-8c02-a66b22e76eac.png)


我自己也在网上买了几个手铐，别问，问就是带情趣俩字的；没意思，一下子就开了，而且和真锁有很大的区别～

9. ### 工牌克隆

  **不用技术的克隆**
  
  ![Uploading image.png…]()

  **工牌的克隆**
  
  ![Uploading image.png…]()

分为两种：高频和低频

![Uploading image.png…]()

一些伪装

![Uploading image.png…]()
![Uploading image.png…]()
![Uploading image.png…]()

10. ### USB攻击

- 键盘记录器（记录所有按键）
- BadUSB
- Bash Bunny
- 橡皮鸭
- WIFI橡皮鸭
- WIFI HID Injector   

