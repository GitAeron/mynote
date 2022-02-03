```
vim ~/.condarc
```

```
proxy_servers:
  http: http://127.09.0.1:5555
  https: http://127.0.0.1:5555
```


<font size=4 color=#EFB752>
vim完毕运行conda isntall时错误，报错信息跟hostname有关，推测Qv2ray代理只代理了http，所以将设置中的代码段</font>

```
https: https:127.0.0.1:5555
```

<font size=4 color=#EFB752>更改为</font>

```
https: http://127.0.0.1:5555
```

<font size=4 color=#EFB752>还有一开始这样设置但是不能使用，推测vim 环境下用tab换行导致格式错误，改用空格进行缩进或者换到文本编辑器环境</font>
