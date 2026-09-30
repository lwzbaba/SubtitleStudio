# 字幕工坊 SubtitleStudio

一个面向 Windows 的本地视频转写与字幕翻译工具。

视频导入、音频提取和 Whisper 语音识别在本机完成；字幕翻译使用用户自行配置的模型 API。

> 当前版本为 Alpha 二进制预览版，暂未公开字幕工坊自身源码，也不是 DeepSeek 官方产品。

## 功能

- 导入常见视频和音频文件
- 在本机提取、分段和识别音频
- 使用 Whisper `large-v3-turbo-q5_0` 模型生成字幕
- 调用用户配置的模型 API 翻译字幕
- 导出标准 SRT 字幕
- 支持任务暂停、取消以及重新打开后继续

## 下载

请在仓库右侧进入 **Releases**，下载最新的 Windows x64 预发布版本。

下载后请核对 Release 中提供的 SHA-256，并完整解压 ZIP。不要将主程序单独移出解压目录。

## 系统要求

- Windows 10/11 x64
- 建议至少 16 GB 内存
- 建议预留 4 GB 以上磁盘空间
- NVIDIA GPU 与兼容驱动可用于 CUDA 加速
- 翻译功能需要网络连接及用户自己的 API Key

## 使用方法

1. 完整解压下载的 ZIP。
2. 确认主程序与 `subtitle-runtime` 文件夹位于同一目录。
3. 运行 `SubtitleStudio-0.1.2-alpha.7.exe`。
4. 在应用中配置模型服务地址、模型和 API Key。
5. 导入视频并创建字幕任务。

## 隐私说明

- 视频、音频处理和语音识别在本机完成。
- 翻译阶段会将待翻译字幕文本及必要上下文发送给用户配置的模型 API。
- 项目不提供公共 API Key，也不会在发布包中附带维护者的个人凭据。
- 请勿在 Issue、截图或日志中公开自己的 API Key、私人字幕或敏感文件路径。

## 安全提示

- 当前主程序尚未进行 Authenticode 数字签名，Windows 可能显示 SmartScreen 警告。
- 只从本仓库的 Releases 下载，并核对 SHA-256。
- DeepSeek Harness 仍处于开发者预览阶段，请勿让程序访问不必要的敏感目录或凭据。

## 使用边界

请只处理自己拥有或已获授权的视频、音频和字幕。不得利用本工具制作、复制或传播违法内容，也不要公开发布未经授权的影视作品、字幕或翻译成品。

## 许可证状态

字幕工坊当前仅发布二进制预览包，暂未授予字幕工坊自身源码的开源许可证。第三方组件分别遵循其原始许可证，完整声明随 Release 压缩包提供。

主要第三方组件包括：

- [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) — MIT
- [whisper.cpp](https://github.com/ggml-org/whisper.cpp) — MIT
- [OpenAI Whisper](https://github.com/openai/whisper) — MIT
- [FFmpeg](https://ffmpeg.org/) — 当前随包构建为 GPLv3
- NVIDIA CUDA Runtime — NVIDIA CUDA Toolkit EULA

## 反馈

如果遇到问题，请在 Issues 中提供：

- Windows 版本
- CPU、GPU 和内存信息
- 操作步骤与错误提示
- 已删除 API Key、字幕正文、私人路径后的日志

请勿上传版权不明的视频、完整字幕、API Key 或其他个人数据。
