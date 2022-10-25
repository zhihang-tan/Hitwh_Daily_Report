# HITwh Daily Report

## 简介

HITwh 工软系统 <sup>[访问入口](http://xy.4009955.com/jktb/)</sup> 上报脚本


## 使用方法

### 关于OPENID
进入**工软校园公众号**，点击**应用中心**，切换到**我的**，如果你是已登录的状态就退出登录，然后跳转进入到这个登录界面

![获取openid的步骤1](https://cdn.jsdelivr.net/gh/zhihang-tan/pictures-private/get_openid1.png)

点**复制链接**，然后查看链接的内容

![获取openid步骤2](https://cdn.jsdelivr.net/gh/zhihang-tan/pictures-private/get_openid2.png)

这样就得到了你的openid

### GitHub Action

1. `Fork` 仓库

2. 设置仓库的 Actions Secrets <sup>[如何设置？](./how-to-enable-actions/#添加-Secrets)</sup>  

   填写好如下表中Secrets

| NAME     | VALUE                   |
| -------- | ----------------------- |
| USERNAME | HITwh工软用户名（学号） |
| PASSWORD | HITwh工软密码           |
| XM       | 中文姓名                |
| XUEYUAN  | 所在学院                |
| OPENID   | openid                  |

**注意**：最好不要直接修改源码里面的信息，信息泄露后果自负

3. 开启 GitHub Actions <sup>[如何开启？](./how-to-enable-actions/#启用-Actions)</sup>

4. 每天早上 ~~06:40 <sup>22:40 UTC</sup>~~ 开启GitHub action 但实际运行大概会延后一个多小时

## 常见错误

### 验证码爬取错误

此错误为硬性错误，忽略即可

![image-20221007111643216](https://cdn.jsdelivr.net/gh/zhihang-tan/pictures-private/daily%20report2.png)

此错误为数据提取错误，需对源码进行修改，需更改提取数据的位置

![](https://cdn.jsdelivr.net/gh/zhihang-tan/pictures-private/dailyreport1.png)
