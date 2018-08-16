---
layout: post
title:  "DC60固件中文指南"
date:   2018-08-15
excerpt: "此贴为DC60的中文指南."
project: true
comments: true
tag:
- keyboard
- dc60
- firmware
- chinese
---

DC60的标配PCB（沉金非蓝牙版本，虚线外设提供）是由QMK驱动，支持一系列的配列。

* 刷固件需要一个固件的 .hex文件，里面有您所需要的配列信息。
* .hex文件可以用QMK原生软件生成（需要懂一些命令行和简单编程），或者网上的工具软件。在这个中文指南里，我会讲解一下用qmk.fm网站刷固件，网址是：[https://config.qmk.fm/#/dc60/LAYOUT](https://config.qmk.fm/#/dc60/LAYOUT)。或者用豆仔的网上刷固件工具。网址是：[http://qmkeyboard.cn/](http://qmkeyboard.cn/)。


### qmk.fm

如果你选择使用qmk官网固件工具，请访问：[https://config.qmk.fm/#/dc60/LAYOUT](https://config.qmk.fm/#/dc60/LAYOUT), 然后参照作者的指引进行 .hex固件的生成。

### kbfirmware.com 或 qmkeyboard.cn

如果你选择使用豆仔网站，请看以下的说明。

#### ANSI 标准配列
* 我先用ANSI和ANSI兼容方向键来做讲解。请先下载Cary提供的这个[json 文件](/assets/firmware/dc60.json) , 并上传到 [刷固件网站](http://qmkeyboard.cn/).
* 上传成功后，会跳转到可编辑配列页面。点击 *KEYMAP*这个按钮，并开始选择每个键所希望对应的字母或者功能。如果需要设置第1层的功能，请将 *MO(1)*在第0层配置给Fn键。
* 字母和功能键都按照您的设想配置好之后，请点击 *COMPILE*来下载配置好的 .hex文件。


#### 左移/minila配列

如果您需要刷左移或者minila版本，请下载使用这个[json 文件](/assets/firmware/dc60_minila.json), 并继续以上的步骤进行刷机.

### 刷机

* 按照并运行[QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases)软件。
* 开始刷固件，请先断开USB线。断开后，按住空格键的同时按住B键，并在此时连接USB线接通键盘到电脑。DC60现在会进入刷机模式。在刷机模式下，在[QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases)软件中点击选择刚才上一步生成的.hex文件，并点击 *flash*来刷机。大概2秒之后，键盘将被刷好，成功！

希望这个说明对您有用，如果有其他问题，请在虚线客制QQ群联系我(oldcat老猫).
