# v2ray_windows_server
v2ray在windows服务器上搭建服务端


##本地操作：

1.首先打开平时在windows上使用的 客户端，左上角服务器->添加vmess服务器，填写你想搭建的服务器的信息，id可以随机生成，最后确定添加

2.右击刚刚的服务器->导出所选服务器为服务端配置，得到一个json文件

##服务器操作：

3.从github中的v2ray-core项目中下载v2ray-windows-32.zip或者v2ray-windows-64.zip，这个是服务端，解压

4.在解压的文件中打开config.json，将第二步的json文件信息拷贝过来，注意！！！注意！！！注意！！！添加access.log和error.log的路径，不然下一步不能运行
例如我随便指定一个路径
"log": {
    "access": "c:/v2ray_log/access.log",
    "error": "c:/v2ray_log/error.log",
    "loglevel": "warning"
  },
  
 5.运行wv2ray.exe即可启动服务端，可以通过任务管理器->服务查看是否有该进程，没有的话大概率是config.json配置文件有错误，还有可能是文件在c盘有运行权限的问题，改到桌面或者其他盘就行了
 
 6.从某一版开始alterId只能为0，不然需要改环境变量，所以直接使用0就好
 
 7.可以愉快上网了
