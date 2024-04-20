# Python ZhipuAI AUR

[English](README.md) | [中文](README.md)

python-zhipuai package for ArchLinux user.

## How to install

Users can install this packages using AUR, it will install the pypi package and depends.

```bash
yay -S python-zhipuai
```

## How to use

Please visit [API Document](https://open.bigmodel.cn/dev/howuse/introduction) to learn how to use.

If you are the first time to use this project, you can visit [Console](https://open.bigmodel.cn/overview) to buy and get your api key.

## Demo

I made a simple demo, you can use the demo to use ZhipuAI LLM in your terminal. If you want to use this demo, you can get your API Key and add your IP address to the whitelist, and you can use it by the following turtorials.

- Features

This demo can get your system language, and it will reply in your system language.

It also works in TTY environment, but TTY works not very well in non-English environment, so TTY will reply you in English.

Subsequently the demo script will continue to be maintained and separated into a separate github project, which I will upload to the AUR and OpenSUSE OBS as the number of users grows.

- Download demo script

```bash
sudo curl -o /usr/local/bin/chatglm https://raw.githubusercontent.com/sengedev/python-zhipuai-aur/main/chatglm
sudo chmod 755 /usr/local/bin/chatglm
```

- Set the system path

Set the `ZHIPU_AI_API_KEY` variable as ZhipuAI API Key.

You can edit `/etc/environment`, and append these messages.
```
ZHIPUAI_API_KEY=<YOUR_ZHIPUAI_API_KEY>
```

- How to use the demo

You can use this command to use the demo.

1. Chat mode
```
chatglm --chat
```

2. Answer mode
```
chatglm "Your Question Here."
```

## Open Source License


This package is the same as upstream and is open source using the MIT protocol, so please follow the open source agreement.

Copyright 2024 sengedev

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
