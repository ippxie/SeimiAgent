# SeimiAgent #
A headless,standalone webkit server which make grabing dynamic web page easier.

[中文文档](https://github.com/zhegexiaohuozi/SeimiAgent/blob/master/zh.md)

# DownLoad #

- [Linux v1.2 x64](http://seimidl.wanghaomiao.cn/seimiagent_linux_v1.2_x86_64.tar.gz)
(support ubuntu14+,centos6+)

- [window7 v1.1 x64](http://seimidl.wanghaomiao.cn/seimiagent_windows7_v1.1_x86_64.zip)

# Quick Start #
```
cd /dir/of/seimiAgent
./seimiagent -p 8000
```
SeimiAgent will start and listen on the port that you set.Than you can use any http client tools post a load reqest to SeimiAgent and get back the content which just like chrome do.Http client tools you can use:
apache `httpclient` of java,`curl` of cmd,`httplib2` of python including, but not limited to.

## Demonstrates ##
![demo](http://77g8ty.com1.z0.glb.clouddn.com/seimiagentdemo.gif)

## Http parameters that seimiAgent support ##
Only support post.Request path:`/doload`
- `url`
your target url

- `renderTime`
How long time you hope to give seimiAgent to process javascript action and document after load finashed.Milliseconds.

- `proxy`
Tell SeimiAgent to use proxy.Pattern:`http|https|socket://user:passwd@host:port`

- `postParam`
Json string only,tell seimiAgent you want to use http post method and pass the parameters in `postParam`.

- `useCookie`
If `useCookie`==1,seimiAgent deem you want to use cookie.Default 0.

- `contentType`
Determine the output format,you can choose `img` or `pdf`,default is `html`.

- `script`
A javascript script which can operate current html document and just seem like in chrome console to execute.

# How to build #
It will take a very long time to build,so it is recommended to use the premade binary file in 'Download'.

##Requirements##
- on ubuntu
```
sudo apt-get install build-essential g++ flex bison gperf ruby perl libsqlite3-dev libfontconfig1-dev libicu-dev libfreetype6 libssl-dev libpng-dev libjpeg-dev python libx11-dev libxext-dev
```

- on centos
```
yum -y install gcc gcc-c++ make flex bison gperf ruby openssl-devel freetype-devel fontconfig-devel libicu-devel sqlite-devel libpng-devel libjpeg-devel
```
## Build ##
```
python build.py
```
Then wait or take a cup of tea.

# More #
More Doc is on his way...
