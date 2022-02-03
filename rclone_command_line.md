## 惯例。As usual.
[rclone mount - official document](https://rclone.org/commands/rclone_mount/)

[nohup 命令](https://www.cnblogs.com/suanec/p/7129164.html)

[Rclone 进阶使用教程 - 常用命令参数详解](https://p3terx.com/archives/rclone-advanced-user-manual-common-command-parameters.html)

[Rclone 使用教程 - 挂载 OneDrive、Google Drive 等网盘(Linux)](https://p3terx.com/archives/linux-vps-uses-rclone-to-mount-network-drives-such-as-onedrive-and-google-drive.html)

[解决Rclone挂载Google Drive时上传失败和内存占用高等问题](https://www.moerats.com/archives/877/)

[如何使用rclone同步远程云盘](https://zhangzr.com/2018/11/08/rclone/)

[记一下rclone同时挂载多个网盘的方法](https://www.b2fun.net/archives/213)

[使用Plexdrive/Rclone+Google Drive搭建无限容量的媒体库，适用于Plex/Emby/Jellyfin等](https://www.moerats.com/archives/870/#%E7%9B%B8%E5%85%B3%E6%95%99%E7%A8%8B)


### 我正在使用的命令

nohup rclone sync -P --stats 1.5s -vv  /od1/  /od2/  >  /home/snoer/2022_02_03_rclone_log 2>1&

ps -aux | grep rclone  这个命令可以查看当前的所有进程，以及UUID，如果出错可以 kill UUID

-P  =  --progress 显示当前的输出，默认是1s刷新一次

--stats 1.5s 控制输出的频率，参数可更改

-v   输出信息，没有vv 详细

-vv  输出全部信息

### rlcone.service参数
##### 以下是一整条命令，先修改DriveName:Folder和LocalFolder的值，再一起复制到SSH客户端运行

cat > /etc/systemd/system/rclone.service <<EOF
[Unit]
Description=Rclone
After=network-online.target

[Service]
Type=simple
User=snoer
ExecStart=/rclone_path mount remote:/path   /local_path   --umask 0000  \
 --default-permissions   \
 --allow-non-empty  \
 --transfers 10   \
 --buffer-size 2000M   \
 --low-level-retries 200   \
 --dir-cache-time 12h   \
 --vfs-cache-mode writes   \
 --vfs-read-chunk-size 5000M   \
 --vfs-read-chunk-size-limit 10G \
Restart=on-abort

[Install]
WantedBy=default.target
EOF
