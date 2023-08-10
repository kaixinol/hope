---
title: 将QQ上的表情包转换为Telegram可以使用的贴纸
date: 2023-08-10 12:18:48
tags:
- Python
- QQ
- Telegram
---
[阿奇(aka Askirin) from @furrystickercn](https://t.me/furrystickercn)  

### Ⅰ. 准备软件

*   安装[Python环境](https://www.python.org/downloads/)
*   安装[waifu2x-caffe](https://github.com/lltcggie/waifu2x-caffe/releases)
*   下载[此Gist](https://gist.github.com/kaixinol/c06983bf9be4302e9f87e20b07102a47)
*   安装[imagine](https://www.nyam.pe.kr/dev/imagine/)

### Ⅱ. 提取原文件

![](https://telegra.ph/file/c8a016d4081164b6a80f7.png)

以此贴纸包为例

点进去任意一个贴纸包的下载界面，点击三个点（_分享到_），再点击复制链接

可以得到以下链接

> https://zb.vip.qq.com/hybrid/emoticonmall/detail?id=233451&traceDetail=base64-eyJhcHBpZCI6Im91dHNpZGUiLCJwYWdlX2lkIjoiNDciLCJpdGVtX2lkIjoiIiwiaXRlbV90eXBlIjoiIn0=

其中，<strong>?id=\<number\></strong>的部分就是我们所需要的代码

打开终端，切换到_qsticker.py_所在的目录

填入我们刚才的得到的代码，按Enter运行

![](https://telegra.ph/file/8c43261d33349515bc9ce.png)

![下载成功](https://telegra.ph/file/a44de43b2287c30e6526d.png)


### Ⅲ. 图片处理及发布

可以看到，原图是单帧静态图像，这里却下载成了gif图片

因此此时需要打开[imagine](https://www.nyam.pe.kr/dev/imagine/)来对图片进行转换

![](https://telegra.ph/file/cf68dd15acbbbda90d233.png)

![](https://telegra.ph/file/02a149d57137b9108c601.png)

这样，我们就得到了可用的贴纸源文件，但这样还不够，因为原图分辨率最高只有300x300，所以需要用[waifu2x-caffe](https://github.com/lltcggie/waifu2x-caffe/releases) 来进行放大

我们打开此软件，并填写以下参数

![](https://telegra.ph/file/69e29b53aace63e0d70c2.png)

其中处理速度设置可以根据自己电脑内存大小来设置

点击_开始_

放大处理完后我们就可以通过[moe\_sticker\_bot](https://t.me/moe_sticker_bot) 来进行发布了

生成后的贴纸包：

[https://t.me/addstickers/ddxkj\_by\_moe\_sticker\_bot](https://t.me/addstickers/ddxkj_by_moe_sticker_bot)

![](https://telegra.ph/file/d95e816fff6c8829ea472.png)