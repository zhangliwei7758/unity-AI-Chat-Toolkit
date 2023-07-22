
# Unity-AI-Chat-Toolkit

这是一个提供给unity开发者的工具库，用于快速实现AI聊天相关功能。目前这个库包含了对chatgpt、rwkv以及chatglm等大语言模型的api调用的代码实现以及实现了微软Azure以及百度AI的语音合成、语音识别的web api接入。在这个库我们可以通过这代码库，在unity上，快速实现跨平台的应用。

![image](https://github.com/zhangliwei7758/unity-AI-Chat-Toolkit/assets/42199471/b214a24e-1fb9-49d3-b405-1a24c9a9ffba)

## unity版本要求

要求unity2020.3.44及以上版本

## 工具内置功能说明

这个工具是根据我之前的AI二次元小姐姐项目整合后的工具包，目前是整合了通用模块，把相关模型包括Vroid以及live2d模型全部删除了，如果需要使用老版本资源的话，文档后面我会放上传送门，自行下载就可以了。

### 项目的主要结构

目前这个工具，主要模块包括LLM以及TTS&&STT两个模块：

![image](https://github.com/zhangliwei7758/unity-AI-Chat-Toolkit/assets/42199471/87a261a6-d266-43c1-936d-5bfa41c72352)

**LLM模块：**实现的就是针对不同的大语言模型的api调用的代码实现。
目前已经实现的大语言模型包括：

① chatgpt: 集成了chatgpt 3.5/4 的api接口，使用这个脚本，需要在脚本参数里填写openai的api key, 默认设置的模型是chatgpt-3.5,如果要替换chatgpt4，需要自行修改模型名称；

② chatglm: 集成了对chatglm官方示例的api接口，如果使用chatglm官方的仓库部署的api服务，就可以直接使用，需要配置的内容是，配置部署好的api地址即可；

③ rwkv: 集成了针对rwkv runner开源项目的api接口，因为rwkv runner这个项目的api格式和chatgpt是一样的，如果下载rwkv runner这个项目使用的话，可以使用工具提供的脚本，只需要在api地址参数配置实际的地址就可以了。

**TTS&&STT模块：**这个模块实现了对语言模型反馈信息的语音合成功能的代码实现，以及发送信息时，可能用到的语音识别服务相关的代码实现。
目前已实现的语音产品包括：

① 微软Azure语音合成以及语音识别服务：如果使用这个服务，需要准备微软Azure的语音服务令牌，自行注册账号，开通服务获得；

② 百度AI的语音合成以及语音识别服务：使用这个服务时，注册百度AI开放平台的账号，开通语音合成、语音识别服务，创建应用获取到相关的密钥，填入相应脚本即可。

### 模型如何使用

示例场景里编写了一个调用示例，查看一下ChatAgent对象。

![image](https://github.com/zhangliwei7758/unity-AI-Chat-Toolkit/assets/42199471/c4e8e414-177b-464e-a5e3-c5922c750717)

在配置面板上，根据自己的需求，配置chatmodel以及tts\stt脚本就可以了。


## 关于发布到WebGL方法

因为这个项目用到了unity内置的microphone类，webgl是不支持这个类的，所以工具也整合了别的大佬的解决方案，具体可在工具包路径下找到Tool,查看具体的配置说明。unity端的代码已经在示例场景做过配置，不需要再处理，只需要在导出的webgl项目中做相应的代码调整即可

![image](https://github.com/zhangliwei7758/unity-AI-Chat-Toolkit/assets/42199471/a42768f2-060f-49da-a42e-08fa31a35c84)


## 旧版本项目传送门

旧版本项目会包含chatgpt\chatglm\微软azure\baiduAI\VITS等几个项目示例，可以以下传送门获取

chatGPTAIGirlFriendSample：https://gitee.com/DammonSpace/chat-gptaigirl-friend-sample

vits-chatgpt-live2d-unity-wife：https://gitee.com/DammonSpace/vits-chatgpt-live2d-unity-wife





