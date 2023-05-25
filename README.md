# LineBotCrawler
use for LineBotCrawler, get group chat message automatic
#程序介绍
该程序用于采集应用程序LINE上群聊消息，主要采集流程为模拟用户登录，模拟用户到达群聊消息界面，获取网页内容，解析其内容获取群聊内容。
#环境安装
所需基本环境
操作系统：LINE数据采集工具可运行在Windows，Macos和Linux上
浏览器：LINE数据采集工具需调用浏览器才可采集数据，可使用Edge或Chrome。
软件环境：python
python安装
可通过官网安装，本文使用的版本为：3.9.7
官网地址：https://www.python.org/
Python安装教程：https://www.cnblogs.com/myx3/p/16269796.html
依赖安装
运行Crawler.py所需要的依赖有selenium，bs4，datetime，以下是依赖安装步骤：
1.	解压LINE.zip后包含以下文件，config为配置文件，Crawler为数据采集程序，requirements为运行程序所需依赖文件。
 
图1解压文件目录
2.	到达解压后的LINE目录安装所需依赖。安装命令：pip install -r requriements.txt若安装失败，可自行通过pip或conda依次进行安装。
注：安装完selenium后需要下载浏览器驱动。
3.	驱动下载。可自行前往以下网址下载驱动文件
Chrome：http://chromedriver.storage.googleapis.com/index.html
Edge：https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/
注：下载的驱动器版本号要与本地浏览器版本号一致。
4.	浏览器版本号查看
Chrome版本号查看，打开浏览器依次进入设置关于Chrome，可看到浏览器版本号。
 
图2Chrome浏览器版本号查看
Edge版本号查看，打开浏览器依次进入设置关于Microsoft Edge，可看到浏览器版本号。
 图3 Edge浏览器版本号查看
#程序配置
配置程序需在config.json文件中进行配置，其主要内容如下：
表1配置文件内容说明
参数	描述
username	开发这平台用户名，即账号，用于登录开发者平台，该账号必须与移动端LINE账号绑定，用于验证
password	开发者平台登录密码
save_path	采集数据的存储路径，文件后缀为json
group_number	采集的群聊个数，即开发者平台添加的群聊和用户个数，这里会自动过滤用户
browser	使用的浏览器，可选为Edge或Chrome
driver_path	驱动路径，这里配置驱动路径，不用添加环境变量也可运行程序。
在配置文件中，以上内容为必填项。
#程序运行
程序运行可在
![image](https://github.com/Guxiguo/LineBotCrawler/assets/56493892/02921ad1-6d66-42de-a1fc-af0777bac09b)

