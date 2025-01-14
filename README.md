<div align="center">
<img src="./assets/img/header.jpg" style="width:80px;height:80px;" />

<h1 align="center">译吁嚱</h1>

<h5 align="center">一个支持Deepl & ChatGPT翻译的网页</h5>

<h6 align="center">青天难上，仍慕青山</h6>
</div>

----

# 特性

- 自动 / 手动 切换夜间模式(Pico.css)
- ChatGPT翻译支持流式输出
- 自动根据译文长度同步拉伸文本框
- 可自由调节原文 / 译文 文本框高度
- 当源语言选定为"自动识别"时，gpt自己识别(随缘)
- 一键复制
- 一键粘贴原文(浏览器需授权读取剪贴板，移动端除Safari外可能无效)
- 悬挂猫一键滚动至顶部
- 甚至能让ChatGPT翻译文言文(源语言选择"文言文")(质量不如文心一言(仅图一乐)
- 日志输出(仅当调用ChatGPT翻译时，可通过日志进行越狱行为审查)(格式：时间 |  IP |  IP位置 |  请求内容[:30])



# 界面预览

## PC

![dark](./screenshot/dark.jpg)

![light](./screenshot/light.jpg)

## Phone

<div style="display: flex;">
<img src="./screenshot/mobie_light.png" alt="mobie" style="zoom: 50%;width:400px;" />
<img src="./screenshot/mobie_dark.png" alt="mobie" style="zoom: 50%;width:400px;" />
</div>

> width < 1100px



# 使用

*开发环境的python版本为3.10.0，理论上py3都可

> 检查python版本：`python --version`
>
> 附：[linux升级python2为python3_python2 升级python3-CSDN博客](https://blog.csdn.net/weixin_40283268/article/details/133797294)
>
> 不明白/嫌麻烦的朋友们可以直接先往下走试试:)



## 运行
1. 下载本项目到本地
   ```bash
   $ git clone https://github.com/GavinGoo/YiXuXi.git
   ```

2. 终端下进入本项目根目录
   ```bash
   $ cd YiXuXi
   ```

3. 安装依赖
   ```bash
   pip install -r requirements.txt
   # （可选）使用venv
   # python -m venv venv
   # ./venv/Scripts/activate # windows
   # source ./venv/bin/activate # linux
   ```

4. 运行
   ```bash
   python main.py --gpt-token <your-gpt-token> --deepl-api <your-deepl-api>
   # 端口默认5000，可通过 --port <port> 更改
   # 更多选项请使用 --help 查看
   ```

5. 浏览器访问`http://127.0.0.1:5000`即可享用:)
   >
   > 另：后台运行：`nohup python ./main.py &`，终端日志会输出到项目根目录下的`nohup.out`
   >
   > ​		关闭后台：`ps aux | grep python`，第二列的数字即进程PID，`kill -9 <PID>`

> 还有很多待完善的地方，在此表示抱歉



# 技巧

1. 通过[DeepLX](https://github.com/OwO-Network/DeepLX)项目(无需token!)作为Deepl接口(感谢`OwO-Network`大佬)

2. 通过`zhile`大佬[wozulong](https://github.com/wozulong)的接口[DeepLX 使用 | FakeOpen Doc](https://fakeopen.org/DeepLX/)作为Deepl接口(可避免"rate limit") & [OpenAI API 相关 | FakeOpen Doc](https://fakeopen.org/Pandora/#openai-api-相关)作为GPT接口(感谢`zhile`大佬)

> 如果使用了大佬的项目/接口，建议修改页面中页脚`footer`的链接&名称



# 感谢

- [DeepLX](https://github.com/OwO-Network/DeepLX)项目`OwO-Network`大佬，项目灵感的起源
- `zhile`大佬[wozulong](https://github.com/wozulong)，fakeopen接口
- [ChatGPT-Web](https://github.com/LiangYang666/ChatGPT-Web)项目，流式输出的实现
- 切图仔群友们
