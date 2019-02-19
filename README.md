#PUSHELL 
公司没买堡垒机，自己想办法解决！ 网上找到了jumpserver(感谢原作者)。于是改了下代码，就有了pushell.
<br/>
运行环境 python2.7.x,mysql
<br/>
####添加功能如下：<br/>
 1.角色: 管理员，审计管理员，监控管理员,配置管理员，普通用户 <br/>
 2.二次验证:增加了token进行验证，令牌生成密码<br/>
 3.增加了URL监控，主机监控 <br/>
 4.集成saltstack <br/>

###使用
pushell启动 <br/>
>![pushelld.py --help](https://github.com/ymc023/pushell/blob/master/screenshot/start_help.jpg)
>![pushell启动](https://github.com/ymc023/PUSHELL/blob/master/screenshot/start_examples.jpg)

>![image](https://github.com/ymc023/PUSHELL/raw/master/screenshot/pushell_token_apk.jpg)
>![登录1](screenshot/pushell_web.jpg)
>![登录2](screenshot/pushell_admin_privileges.jpg)

###安装
<br/>
1.git 代码 
>![git clone](screenshot/11.jpg) 
>![0](screenshot/2.jpg)
>![1](screenshot/3.jpg)
>![2](screenshot/4.jpg)
>![3](screenshot/5.jpg)




您好 环境已经搭建完了，但是不知道token验证码，登录不了，怎么获取验证码，求大神指点？？？
你好，代码内置的key是：NFP7DMPDPEFK6I6S ,你可以在手机上使用 freeotp软件，添加这个key,生成的token就可以正常验证了，二次认证路径pushell/two_auth.py 你可以自行修改
class TwoAuth():
def **init** (self,secret='NFP7DMPDPEFK6I6S'):
self.secret = 'NFP7DMPDPEFK6I6S'
self.totp = pyotp.TOTP(secret)
def gen_token(self):


请问pushell token这个工具怎么下载
这个是自己改的，应用市场上没有，手机你可以使用freeotp,或是google authenticator, chrome 可以使用OTP Safe for Chrome，任何OTP开源软件都可以
