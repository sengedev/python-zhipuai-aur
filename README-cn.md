# Python ZhipuAI AUR

[English](README.md) | [中文](README-cn.md)

为ArchLinux用户打包的python-zhipuai 软件包

AUR 仓库: https://aur.archlinux.org/packages/python-zhipuai

## 如何安装

用户可以使用以下命令安装这个软件包，这个命令会同时安装pypi包及其依赖。

```bash
yay -S python-zhipuai
```

## 如何使用

请参阅 [API文档](https://open.bigmodel.cn/dev/howuse/introduction) 来获取API的调用方式。

如果您是第一次使用，您可以访问 [个人中心](https://open.bigmodel.cn/overview) 来获取API密钥。

## Demo

我同时打包了一个简单的Demo，用户可以将使用这个Demo在终端中体验ZhipuAI的大语言模型。如果您想要体验这个Demo，您可以获取API Key后将您的IP地址添加到白名单，然后即可参考上述的教程来进行体验。

- 程序特征

程序会自动获取系统所处的语言环境，并使用当前的系统语言来回答问题。

其中，程序也支持在TTY中使用，但是TTY不支持中文显示，所以TTY环境下，系统会使用英文来进行回答。

后续该demo脚本会继续维护并分离为一个单独的github项目，在用户数量增长后我会上传该项目到AUR和OpenSUSE OBS中。

- 下载demo脚本

```bash
sudo curl -o /usr/local/bin/chatglm https://raw.githubusercontent.com/sengedev/python-zhipuai-aur/main/chatglm
sudo chmod 755 /usr/local/bin/chatglm
```

- 设置环境变量

将`ZHIPU_AI_API_KEY`变量设置为zhipuai的API Key

您可以编辑`/etc/environment`，然后在该文件中追加 以下内容
```
ZHIPUAI_API_KEY=<YOUR_ZHIPUAI_API_KEY>
```

- 使用方法

您可以使用以下命令来体验zhipuai的api.

1. 聊天模式
```
chatglm --chat
```

2. 问答模式
```
chatglm "Your Question Here."
```

## 开源协议

该软件包和上游相同，使用MIT协议开源，请遵守开源协议。

Copyright 2024 sengedev

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
