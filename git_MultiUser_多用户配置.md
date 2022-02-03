<font size=6 color=#EFB752>Step 1: 要运行以下代码，生产一对密钥</font>

```C
ssh-keygen -t rsa -C "EMail"
```

<font size=5 color=#EFB752>其中mail替换成自己的邮件，或者github设置中的隐藏邮件.然后会得到一下结果</font>

```
(base) [15:55:07] [~] ❱❱❱ ssh-keygen -t rsa -C "youremail@gmail.com"

Generating public/private rsa key pair.

Enter file in which to save the key (/home/snoer/.ssh/id_rsa):
```

<font size=5 color=#EFB752> 到这一步就要注意了，这里是自定义文件名称，因为是多用户，每个用户都是不同的密钥文件。 </font>

<font size=5 color=#EFB752>所以这个步骤执行两次，文件名记得更改，就生成好了ssh密钥。 </font>

<font size=6 color=#EFB752>Step 2: 到github页面登录自己的帐号，然后进入 setting -> SSH and GPG keys 添加刚刚生产的公钥，结尾是.pub</font>

```C
cat  name_rsa.pub
```

<font size=6 color=#EFB752> Step 3: 到.ssh文件夹编辑config文件，配置多用户。 </font>

```
cd /home/user_name/.ssh/
vim config
```

<font size=5 color=#EFB752> 以下代码段是配置信息，别拼错了，尤其是IdentityFile </font>

```C
Host aeron
  HostName github.com
  User aeron
  IdentityFile ~/.ssh/aeron_rsa

Host snoer
  HostName github.com
  User snoer
  IdentityFile ~/.ssh/snoer_rsa


填写说明：
Host 　　主机别名,可以自定义。
HostName　服务器真实地址
User　用户名,随意。
IdentityFile　　私钥文件路径
PreferredAuthentications　　认证方式 可不填写
```

<font size=6 color=#EFB752>Step 4: 检查配置是否成功后，就完事了。</font>

```C
ssh -T git@aeron
```
<font size=5 color=#EFB752>这里的git@aeron,将 aeron 替换成 config 文件中 Host 那段配置填写的主机别名。</font>
