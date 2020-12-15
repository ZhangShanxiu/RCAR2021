# RCAR2021web
website of RCAR2021

## 系统设置

### Install Packages
1. Install Nodejs 

    `sudo apt-get install nodejs`

2. Install npm

    `sudo apt-get install npm`

3. Config Taobao registry

    `npm config set registry https://registry.npm.taobao.org`

4. Update Nodejs

    `npm i -g n`

    `n latest`
    
    Reload cmd shell

5. Install pm2

    `npm i -g pm2`

6. Install Mongodb

    `sudo apt-get install mongodb-server`

8. Install Nginx

    `sudo apt-get install nginx`

9. Install certbot

    `sudo apt install -y nginx certbot python-certbot-nginx`

### Setup 
1.  从备份的数据文件夹中恢复数据到本地数据库

    `cd src`

    然后恢复数据:

    `mongorestore`

2. 分别cd到 `admin` ， `desktop` ， `web` 和 `server` 文件夹中，然后 `npm i`， 再然后编译`npm run build`。

    以`admin`例：

    `cd admin`

    `npm i`

    `npm run build`

    *ps:* 把`npm run build`改为`npm run server`可以在本地测试网站效果

3. run web in localhost://3000

    `cd server `

    `pm2 index.js`

    vist your server public ip + port3000   
    
    ip:3000



### Config

1. 在线配置nginx：

    [Go Nginx config](http://nginxedit.cn)

2. 根据要求依次选择相应的
    - **网站配置**选项：Preset，域名等等
    - **全局配置**选项：刚开始基本不用管

3. 下载/复制config文件

4. 把config文件复制到服务器的`/etc/nginx/sites-available/`文件夹中，再在`/etc/nginx/sites-enabled/`中创建一个软连接指向`/etc/nginx/sites-available/`中的config文件

    例如域名为`test.com`：
    `cp sites-available/test.com.conf /etc/nginx/sites-available/`

    `cd /etc/nginx/sites-avaible`

    `sudo ln -s ../sites-available/test* /etc/nginx/sites-enabled/` 

5. !! Change me@example.com to your email
    `sudo certbot --non-interactive --redirect --agree-tos --nginx -d test.com -m me@example.com`



## 说明
一共有3个端口 admin是管理员后台界面 desktop是桌面版的界面 web是手机版的界面 src里是一些图片 视频 server里是最终的启动文件


## Administrator
username : siat / admin

password : siatsiat

## Remark
如果要编译成静态html文件，可以直接打开的，需要把对应文件夹里的`vue.config.js`（如：`desktop/vue.config.js`）中的`publicPath`的`/`改为`./`。

[vue-cli 3.0打包之后可以本地访问index.html](https://blog.csdn.net/qq_42852004/article/details/94397291)

## 配套学习资料
- [NodeJs + VueJs (Express + ElementUI) 全栈开发王者荣耀手机端官网和管理后台](https://www.bilibili.com/video/BV1A4411Y7fi?p=2)
- [视频源码](https://github.com/wxs77577/node-vue-moba)