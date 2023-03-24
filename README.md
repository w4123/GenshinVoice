# GenshinVoice

此处包含原神中直接提取出的所有语音文件和对应的文字文本。

已更新3.5版本内容。result.json中包含82924条记录（部分记录所对应的实际音频文件已被删除，这些记录也没有对应的文本信息）。其中77965条包含text文本记录，81945条包含npcName名称记录。

如果发现条目错误或者以下情况的条目，请提交issue：
1. 条目中缺失npcName或者text，并且
2. 对应的语音文件确实存在（或者在历史版本中存在-请告知版本），并且
3. 语音文件确实对应着某个NPC或者含有有用的文字信息（部分角色语音，如攻击和受击时的角色音效，不包含有用的文字信息，因此不会有text）

你也可以向本项目提出PR贡献内容：
1. 将含有#的text内容替换为语音中实际上说出的内容，放置到cleaned_text项中。

使用注意事项：
1. **请注意所有wav文件均保留了原有采样率和声道信息，不同文件的采样率和声道数可能不同。**
2. 相同角色可能有不同的npcName，比如流浪者和#{REALNAME[ID(1)|HOSTONLY(true)]}，菲谢尔和幽夜菲谢尔等。其中一种判断方式是通过文件名称中的角色名称来判断实际角色。
3. text中可能包含以#开头的文本，其中内容含有游戏内替换项（比如替换成玩家名字或不同人称代词等）。

result.json format:
```json
{
    "00000405dad50548": {
        "fileName": "English (US)\\VO_friendship\\VO_xingqiu\\vo_xingqiu_dialog_greetingNight.wem", // 原始文件名 Original Filename
        "language": "EN", // EN/CHS/KR/JP Language 语言
        "npcName": "Xingqiu", // Name of the character in the corresponding language 角色名称，请注意会以对应的语言显示
        "text": "What say you we snatch a few fireflies and read in the light they give? Hehe... Hey, I'm joking. Seriously, don't, it's bad for your eyesight.", // Text content of the voice file 文件文本内容
        "type": "Fetter" // Dialog/Fetter/AnimatorEvent/WeatherMonologue/JoinTeam/DungeonReminder/Card Type of the voice file 语音类型
    },
    "..." : {
    },
}
```

wav文件压缩包含有所有提取出的语音文件。文件路径为原始文件路径。根目录下还有NoData文件夹代表未从游戏数据里获取到任何相关信息的语音文件。

wav zip file consists of all extracted voice files. The file paths follow the original file paths. There is also a NoData folder at the root directory that represents all files extracted that cannot match to any game data.

This repository contains all voice audio files and corresponding NPC names and texts from Genshin Impact.
All files are extracted directly from the game.

链接 Link： [点击此处 Click Here](https://kokona-my.sharepoint.com/:f:/g/personal/suhui_kokona_tech/Erk1kf9NgF5CqBVnINIrWKUBg_T-7FrM98Z-hX227jiTOA?e=3qAefT)

文件正在更新中，暂时只包含中文，但会最后包含所有四种语言的文件。

The files are being updated. Currently, only the Chinese version is available but all four languages will be uploaded eventually.

不包含任何测试版/泄露版信息。

This repo contains no info regarding leak/beta versions.

请注意所有音频版权属于米哈游，此处分享仅做学习用途。

Please note that all copyrights belong to Mihoyo/Hoyoverse. These files are only shared here for educational purposes.

使用这些文件的所有后果将由使用者承担，溯洄不负任何责任。

The user of these files bears all consequences for using these file. The repo maintainer bears no responsibility.

请勿在无米哈游书面授权的情况下将它们用于商业用途。

Please do not use these files for commercial purposes without a prior written consent from Mihoyo/Hoyoverse.

如果你在自己的视频/项目等中使用了这些文件，推荐注明文件来源以及整理者。

If you use these files in your own project/video etc., it would be appreciated if you credit the repo maintainer.

PS: 如果米哈游希望删除此repo，可以在Issues中联系我。

PS: If Mihoyo/Hoyoverse wishes this repo to be deleted, please contact me via Issues.
