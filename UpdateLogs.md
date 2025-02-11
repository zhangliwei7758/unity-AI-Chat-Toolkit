# 项目更新日志

## 2025.2.11 update
### 新增功能
1、新增对DeepSeek的接口对接模块，能够利用DeepSeek来驱动AI小姐姐聊天


## 2024.9.30 update
### 新增功能
1、新增对百度AppBuilder的接口对接模块，能够利用百度千帆Agent来驱动AI小姐姐了

## 2024.4.27 update
### 新增功能
1、新增对Ollma部署的本地大模型的api调用支持模块，可以实现Ollama驱动聊天了


## 2024.4.22 update
### 新增功能
1、新增对GPT-SoVITS项目[GPT-SoVITS-beta0306fix2]版本的API接口对接支持模块，可以实现局域网访问了
2、更新了gradio api的接口代码，兼容当前版本


## 2024.1.25 update
### 新增功能
1、新增对GPT-SoVITS项目的API接口对接支持模块

## 2023.12.27 update
### 更新接口
1、百度千帆大模型平台知识API接口代码同步更新

## 2023.12.11 update
### 新增功能
1、新增对百度千帆大模型平台知识库相关功能的api接口支持模块

## 2023.11.20 update
### 新增功能
1、新增OpenAI的TTS服务的api支持模块，可实现对接openAI语音合成服务，实现文字转音频功能

## 2023.10.30 update
### 新增功能
1、新增智谱AI开放平台的api支持模块，可实现chatGLM Turbo模型的api调用

## 2023.10.4 update
### 新增功能
1、增加语音唤醒功能，新建WOV基类，用于维护语音唤醒解决方案。本次更新，新增了unity自带的windows.speech库下的关键词识别的代码实现，可以在windows平台下，实现关键词唤醒功能

2、增加了实时语音聊天对话示例场景，可以在Scene文件夹下，找到相应的示例场景

## 2023.9.17 update
### 新增功能
1、增加语音合成模式选项，可在ChatAgent对象脚本设置，是否通过语音合成
### 修复缺陷
1、修复chatgpt-turbo脚本，在调用api时，反馈{"message": "We could not parse the JSON body of your request. (HINT: This likely means you aren't using your HTTP library correctly. The OpenAI API expects a JSON payload, but what was sent was not valid JSON.}的问题

## 2023.9.8 update
### 新增功能
1、增加百度智能云千帆大模型平台的公共服务模型api支持，包括：
ERNIE_Bot,
ERNIE_Bot_turbo,
BLOOMZ_7B,
Qianfan_BLOOMZ_7B_compressed,
ChatGLM2_6B_32K,
Llama_2_7B_Chat,
Llama_2_13B_Chat,
Llama_2_70B_Chat,
Qianfan_Chinese_Llama_2_7B,
AquilaChat_7B,

## 2023.8.22 update
### 新增功能
1、增加针对科大讯飞的语音服务，包括语音识别以及语音合成模块

2、增加星火大模型V1.5以及V2.0的api集成模块，可使用星火大模型的api进行聊天应用

## 2023.8.11 update
### 新增功能
增加了针对whisper-webservice这个项目的api集成代码，部署下面这个项目，可以通过本次更新的代码调用语音识别的api
https://github.com/ahmetoner/whisper-asr-webservice
## 2023.8.6 update
### 新增功能
1、集成了Oculus的口型插件，AI小姐姐语音对话的时候，可以实现对a i u e o五种元音的识别和口型映射了。
[注意：因为Oculus插件包比较大,所以源码里只保留了window的dll库，针对安卓以及IOS的库，需要的话请自行下载，并放入tool/LipSync下的plugins文件夹]
### 修复缺陷
1、修复了百度语音合成脚本，使用的app key未授权语音合成服务时，返回信息类型不能正确处理，并打印的问题

## 2023.7.27 update
### 新增功能
1、集成openai的whisper语音识别api，实现语音识别功能
2、增加webgl平台中文输入解决方案[全屏无效，暂无其他好的解决方案]

## 2023.7.24 update
### 修复缺陷
1、修复百度语音合成脚本，获取token异常，以及语音识别精度低的问题

## 2023.7.22 create
创建本仓库，提供unity调用大语言模型api以及相关语音服务api的插件，主要功能：
### 新增功能
**LLM大语言模型交互**
1、集成chatgpt的api，实现chat聊天功能
2、集成chatglm官方接口格式的api，实现chat聊天功能
3、集成rwkv runner项目的api，实现chat聊天功能
**语音模型交互**
1、集成Azure语音服务api，实现语音合成以及语音识别功能
2、集成百度AI开放平台语音服务api，实现语音合成与语音识别功能
**其他**
1、增加发布WebGL，实现语音录制解决方案的代码，实现在webgl端的录音功能



