[size=150][/size] [b]Before Start to read this post, I have to say sorry about that I might be post in a wrong forum section... So If you're a admin, Pls correct it.
[/b]
   My only purpose is to help people who has the same trouble with me....... So It's not a post for asking help, But I also think it's not about a tutorial post.....
   I search on google for one week, spend almost whole day to fix these problem, tried any suggestion on google search result.
   Finally I solved this problem myself.. I fixed this problem 3 times, and using different way to fixed it each time..
Oh by the way, My English is poor, however it's good than my GNU/Linux knowledge(just start last week..

  So if you have the same situation or try to find a way to fix these problem
          "The Brightness Control can't work after installing Nvidia Driver"
          "The Brighrness Control after just installed Linux Mint 20.3(Una),  Linux Mint 20.2, Linux Mint 20.1 or Linux Mint 20.0"

Then you can continue to read, and trust me, it will works. Don't lose your faith, you can fix it ! Cheer up!

The first of all, my info.
  [code]System:    Kernel: 5.13.0-28-generic x86_64 bits: 64 compiler: N/A Desktop: Cinnamon 5.2.7
           wm: muffin dm: LightDM Distro: Linux Mint 20.3 Una base: Ubuntu 20.04 focal
Machine:   Type: Laptop System: LENOVO product: 82B6 v: Lenovo Legion R7000 2020 serial: <filter>
           Chassis: type: 10 v: Lenovo Legion R7000 2020 serial: <filter>
           Mobo: LENOVO model: LNVNB161216 v: SDK0L77769 WIN serial: <filter> UEFI: LENOVO
           v: EUCN22WW date: 08/07/2020
Battery:   ID-1: BAT0 charge: 50.1 Wh condition: 52.2/60.0 Wh (87%) volts: 17.0/15.4
           model: Celxpert L19C4PC0 serial: <filter> status: Unknown
CPU:       Topology: 6-Core model: AMD Ryzen 5 4600H with Radeon Graphics bits: 64 type: MT MCP
           arch: Zen rev: 1 L2 cache: 3072 KiB
           flags: avx avx2 lm nx pae sse sse2 sse3 sse4_1 sse4_2 sse4a ssse3 svm bogomips: 71862
           Speed: 3988 MHz min/max: 1400/3000 MHz Core speeds (MHz): 1: 3986 2: 3955 3: 1407
           4: 1397 5: 1772 6: 1774 7: 1774 8: 1774 9: 1554 10: 1414 11: 1261 12: 1297
Graphics:  Device-1: NVIDIA vendor: Lenovo driver: nvidia v: 470.86 bus ID: 01:00.0
           chip ID: 10de:1f99
           Display: x11 server: X.Org 1.20.13 driver: nvidia resolution: 1920x1080~60Hz
           OpenGL: renderer: NVIDIA GeForce GTX 1650/PCIe/SSE2 v: 4.6.0 NVIDIA 470.86
           direct render: Yes
Audio:     Device-1: NVIDIA driver: snd_hda_intel v: kernel bus ID: 01:00.1 chip ID: 10de:10fa
           Device-2: AMD Raven/Raven2/FireFlight/Renoir Audio Processor vendor: Lenovo driver: N/A
           bus ID: 05:00.5 chip ID: 1022:15e2
           Device-3: AMD Family 17h HD Audio vendor: Lenovo driver: snd_hda_intel v: kernel
           bus ID: 05:00.6 chip ID: 1022:15e3
           Sound Server: ALSA v: k5.13.0-28-generic
Network:   Device-1: Realtek RTL8111/8168/8411 PCI Express Gigabit Ethernet vendor: Lenovo
           driver: r8169 v: kernel port: 1000 bus ID: 03:00.0 chip ID: 10ec:8168
           IF: eno1 state: down mac: <filter>
           Device-2: Intel Wi-Fi 6 AX200 driver: iwlwifi v: kernel port: 1000 bus ID: 04:00.0
           chip ID: 8086:2723
           IF: wlp4s0 state: up mac: <filter>
Drives:    Local Storage: total: 1.38 TiB used: 9.69 GiB (0.7%)
           ID-1: /dev/nvme0n1 vendor: Micron model: MTFDHBA512TDV size: 476.94 GiB
           speed: 31.6 Gb/s lanes: 4 serial: <filter>
           ID-2: /dev/sda vendor: Seagate model: ST1000LM035-1RK172 size: 931.51 GiB
           speed: 6.0 Gb/s serial: <filter>
Partition: ID-1: / size: 261.46 GiB used: 9.54 GiB (3.6%) fs: ext4 dev: /dev/nvme0n1p6
           ID-2: /boot size: 923.0 MiB used: 124.4 MiB (13.5%) fs: ext4 dev: /dev/nvme0n1p3
           ID-3: swap-1 size: 7.45 GiB used: 0 KiB (0.0%) fs: swap dev: /dev/nvme0n1p5
USB:       Hub: 1-0:1 info: Full speed (or root) Hub ports: 4 rev: 2.0 chip ID: 1d6b:0002
           Device-1: 1-2:2 info: SHARKOON 2.4G Mouse type: Mouse driver: hid-generic,usbhid
           rev: 1.1 chip ID: 1ea7:0064
           Device-2: 1-3:3 info: Syntek Integrated Camera type: Video driver: uvcvideo rev: 2.0
           chip ID: 174f:244c
           Hub: 2-0:1 info: Full speed (or root) Hub ports: 2 rev: 3.1 chip ID: 1d6b:0003
           Hub: 3-0:1 info: Full speed (or root) Hub ports: 4 rev: 2.0 chip ID: 1d6b:0002
           Hub: 3-1:2 info: Genesys Logic 4-port hub ports: 2 rev: 2.1 chip ID: 05e3:0610
           Device-3: 3-1.1:4 info: GenesysLogic USB2.1 Hub type: Keyboard,HID
           driver: hid-generic,usbhid rev: 2.0 chip ID: 258a:0190
           Device-4: 3-3:3 info: Intel type: Bluetooth driver: btusb rev: 2.0 chip ID: 8087:0029
           Device-5: 3-4:5 info: Integrated Express ITE Device(8910) type: Keyboard
           driver: hid-generic,usbhid rev: 2.0 chip ID: 048d:c100
           Hub: 4-0:1 info: Full speed (or root) Hub ports: 2 rev: 3.1 chip ID: 1d6b:0003
           Hub: 4-1:2 info: Genesys Logic USB3.2 Hub ports: 2 rev: 3.2 chip ID: 05e3:0620
Sensors:   System Temperatures: cpu: 49.5 C mobo: N/A gpu: nvidia temp: 42 C
           Fan Speeds (RPM): N/A
Repos:     No active apt repos in: /etc/apt/sources.list
           Active apt repos in: /etc/apt/sources.list.d/google-chrome.list
           1: deb [arch=amd64] https: //dl.google.com/linux/chrome/deb/ stable main
           Active apt repos in: /etc/apt/sources.list.d/official-package-repositories.list
           1: deb http: //packages.linuxmint.com una main upstream import backport
           2: deb http: //archive.ubuntu.com/ubuntu focal main restricted universe multiverse
           3: deb http: //archive.ubuntu.com/ubuntu focal-updates main restricted universe multiverse
           4: deb http: //archive.ubuntu.com/ubuntu focal-backports main restricted universe multiverse
           5: deb http: //security.ubuntu.com/ubuntu/ focal-security main restricted universe multiverse
           6: deb http: //archive.canonical.com/ubuntu/ focal partner
Info:      Processes: 331 Uptime: 33m Memory: 7.63 GiB used: 2.01 GiB (26.3%) Init: systemd v: 245
           runlevel: 5 Compilers: gcc: 9.3.0 alt: 9 Client: Unknown python3.8 client inxi: 3.0.38
[/code]

And further info:
   Legion Y7000(2020)   CPU: AMD Ryzen 4600H  GPU: AMD Radeon / Nvidia Geforce GTX 1650
   I have 2 EFI on my PC.
     One is Win10 21H2(Family)
     Another is Linux mint 20.3 Una - Cinnamon (X64 or amd64)

So let's Start my story........

The First Step:
    After install Linux mint by USB, And reboot to My Linux mint 20.3 on PC...........I can't come into my desktop, and my screen is black with some word, I don't know how to describe it.
    If your situation is the same like me........ Dont worry about it....
    Before you choose Linux mint 20.3 on GNU pannel to start, you can press 'e' to modify some setting....  You need to see this picture. I find a proper one: https://supportkb.dell.com/img/ka02R000000i0LDQAY/ka02R000000i0LDQAY_en_US_5.jpeg
    You guys might be know what to do.  
    Yes,  delect "quiet splash" and enter "nomodeset" to replace it.
Then, you can come into your desktop. But I'm sure you guys search it on google and fixed it already.

OK, Let's go to Second Step:

  Before this following, you might need to update Linux kernel, no matter the default 5.4.* or other..
  This action is full of argue !!!! I am just a starter, do your own choice, Just Becareful.  
  The default kernel also not work, so I update mine. and the default is older than my pc...

    If you are just installed Linux mint 20.3, don't change software source(back to default source).

    And open your terminal(Ctrl + Alt + T), enter
    sudo su
    apt-get install vim
    (just for install vim, if you're use vi, it's also fine.)

    Then install proper "NVIDIA driver", use "Driver Manage" to install it.(by this way, it will block nouveau aotumaticlly.)
