# HoshinoBot增强-语音调用支持

*****

## 简介

适用于 [HoshinoBot](https://github.com/Ice-Cirno/HoshinoBot) 的功能性增强，
通过修改 ``R.py`` 文件来实现直接通过 R模块 调用语音的功能

以下环境下已经过测试：
- [x] ``python 3.8.5 32&64bit``
- [x] ``python 3.8.9 32&64bit``
- [x] ``HoshinoBot V2.0``
- [ ] 理论上支持``nonebot 1.6.0+``，``python 3.9``

#### 使用例：

调用图片（原）
```python
xxx = R.img(xxx/xxx.jpg).cqcode

@sv.on_fullmatch(["发送图片"])
async def xxx(bot, ev):
  await bot.send(ev, xxx)
```

**调用语音**
```python
xxx = R.rec(xxx/xxx.mp3).cqcode

@sv.on_fullmatch(["发送语音"])
async def xxx(bot, ev):
  await bot.send(ev, xxx)
```

原理是使用 ``nonebot`` 的 ``MessageSegment`` 模块，所以 MessageSegment 支持的语音文件格式理论上都可以调用。

*****

## 安装

直接替换 **R.py** 文件即可。

*****

### 其它

因为之前的插件大量使用绝对路径 （类似这种：[CQ:record,file=xxx]） 被人吐槽，所以简单修改了一下
本人非专业程序员，业余写着玩玩，代码很菜，大佬们看看就好QwQ。

made by [Soung2279@Github](https://github.com/Soung2279/)

### 鸣谢

[HoshinoBot项目地址](https://github.com/Ice-Cirno/HoshinoBot)
