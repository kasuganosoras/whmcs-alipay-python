# python版的 whmcs 的支付宝免签接口

依赖：python，pyquery,requests

使用 pip 进行第三方库的安装
```shell
pip install pyquery
pip install requests
```

## 使用方法：
先安装依赖，whmcs 安装 whmcs 文件夹里面的接口文件。并填写 key

填写 alipay.py 里面的信息：

- key
- api
- 接收邮件和发送邮件的邮件，密码
- cookies 的 ALIPAYJSESSIONID

建议使用 screen 进行守护，没有的话也可以。

`python alipay.py` 跑起来，screen 后台运行就好。

## 关于ALIPAYJSESSIONID的说明：

登陆 https://lab.alipay.com/consume/record/items.htm

打开开发者工具（F12）里面的 console，输入 `document.cookie`

将 ALIPAYJSESSIONID 的值尽快复制到 alipay.py 里面，并尽快跑起来。
	
## Thank：
whmcs 的接口来自 https://github.com/qibinghua/whmcs_alipaypersonal
