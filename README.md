<br>

<p align="center">
    <img alt="PivotAIOS" src="./docs/assets/GalaxyAI-logo.png" width="300px"/>
</p>
<br>

# PivotAIOS · 天枢大模型操作系统

> 算网为基，天枢为擎，赤潮出征——共建 Token 经济生态 | 智能平权 · 解放创造力

#### 介绍

PivotAIOS（天枢大模型操作系统）是以多模态大模型为核心的新型 AI 操作系统：集成大模型内核与智能体应用，混合大模型架构同时支持云端与本地大模型，为各类 Agent 提供标准化开发、部署与运行环境，实现大模型与智能体应用开箱即用。

系统围绕 AI 大模型技术构建，专为大模型应用全生命周期（部署、推理、迭代、运维）设计，核心价值是"为大模型落地提供端到端的标准化支撑环境"，解决"模型与硬件、场景与工具、安全与效率"的协同难题，原生集成依赖管理、资源调度、模型服务、智能体和知识库等工具，针对主流 AI 框架（如 PyTorch）和大模型推理引擎进行内核级、库级的深度优化，大幅降低部署和运维复杂度，实现"智能平权、解放创造力"的 AI 共生体，开启人机共生的新纪元：

1. **专用性**：聚焦大模型推理场景，如针对模型服务的分布式算力调度、针对推理的低延迟优化；
2. **模型应用全生命周期覆盖**：从模型管理到模型部署上线、升级迭代、安全运维，提供一站式支撑，避免企业拼接多工具的"碎片化"困境；
3. **生态兼容性**：既兼容开源生态（如 Hugging Face 模型库、GitHub 社区工具），也支持商业生态（如厂商闭源模型、企业智能体应用商店），平衡开放与安全。

#### 天枢模坊（Pivot Model Studio）

天枢模坊是基于开源开放的 PivotAIOS 构建的大模型客户端（Electron 桌面应用），使用本地算力，可视化快速一键部署本地大模型，开箱即用的 AI 原生 OS 体验：

- **本地运行时**：WSL2 + K3s + Docker + NVIDIA Container Toolkit 自动初始化，通过 K3s 调度 llama.cpp / vLLM / ollama 等大模型推理引擎，充分利用本地 GPU；
- **可视化操作**：模型市场、模型下载、一键部署、资源规格自定义、OpenAI 兼容 API 调用等全部所见即所得；
- **数据安全**：数据全程在用户自有终端流转，本地模型处理的数据默认不上传云端；
- **激励机制**：创新积分激励机制，将用户贡献量化确权，实现"共建平台、共享增值"的红利分配。

客户端仓库详见 [pivotai-modelstudio](../pivotai-modelstudio)。

#### 软件架构

核心构成：三层架构支撑全流程能力

1. **内核层**：基于 Linux 内核扩展 AI 专用模块，支持异构计算（GPU/TPU/NPU）、模型运行工具链（GPU 驱动/CUDA/PyTorch）、大模型内存和存储管理等；
2. **平台层**：集成推理引擎/微调框架，提供经过认证的模型库，包含性能优化（TensorRT/ONNX 加速）、RAG/向量数据库/langchain/MCP 等组件和 SDK，支持容器部署和云边部署、模型可观测等能力；
3. **应用层**：提供主流的智能体/工作流工具和应用，AI 应用市场中包括 ComfyUI/dify/知识库等常见的主流应用。

### 核心特性

- **全栈开源的智能底座**：提供统一的操作系统内核和开发框架、编排调度系统、开发环境，支持 k8s、Ray、Docker，助力 AI 应用快速集成开发。
- **性能优化的推理引擎**：支持经过优化的多推理引擎，如 llama.cpp、vLLM、Triton、BentoML 等，支持 Transformer、Diffusion、MOE、Lora 等主流的算法架构。
- **包含丰富的开源模型**：模型市场预集成开源模型（如 Llama3、Qwen、DeepSeek、SD、FLUX、Whisper 等），覆盖大语言模型、文生图扩散模型、STT 与 TTS 语音模型、多模态模型等，支持百亿至万亿级参数模型。
- **完善的开源工具链**：集成 Langchain、dify、RagFlow、Milvus 等工具链和中间件，可帮助开发者极大提高 AI 应用开发效率。
- **多智能体协同引擎**：通过 MCP 协议实现自然语言处理（NLP）、计算机视觉（CV）、语音交互等能力的协同调用。例如，文本生成模型可联动文生图模型完成系列漫画的制作。
- **广泛的兼容性**：支持 Apple Mac、Windows 和 Linux 不同的 OS 和 NVIDIA、AMD GPU，轻松添加异构 GPU 资源。
- **OpenAI 兼容 API**：提供兼容 OpenAI 标准的 API 服务。
- **用户和 API 密钥管理**：简化用户和 API 密钥的管理流程。

### 主要特点

- **效益优势**：将普通 PC 变成 AIPC，无限 token，摆脱云端按 Token 计费的"按量付费"模式，可降低使用 AI 模型的成本；
- **模型丰富**：聚合海量开源模型，覆盖对话、绘画、语音、视频等领域，按需部署、随心切换；
- **极简部署**：所见即所得，拖拽式可视化界面，模型自动匹配显存大小，10 分钟即可完成模型部署与服务发布；
- **数据安全**：数据全程在用户自有终端流转，从物理层面隔绝泄露风险，实现绝对的隐私可控与合规溯源；
- **激励机制**：创新积分激励机制，将用户贡献量化确权，实现"共建平台、共享增值"的红利分配；
- **生态共创**：开源引擎驱动，汇聚社区智慧，通过社区驱动持续进化，开放理念共创共建价值网络。

## 安装

### Windows（天枢模坊客户端，推荐）

安装包下载地址（官网下载页同步更新）：

[天枢模坊客户端 Windows 安装包](https://dl.bartplanet.ai/tianshu-models/windows)

运行安装包后自动完成：

1. **WSL2 环境**：自动启用 WSL2 + 安装 Ubuntu 发行版（内部命名 `PivotAIOS`）；
2. **运行时初始化**：安装 Docker + NVIDIA Container Toolkit + K3s + NVIDIA Device Plugin（安装包内置离线资源缓存，避免国内网络拉取失败）；
3. **GPU 验证**：自动验证宿主 GPU 在 Docker 和 K3s 中均可用；
4. **启动客户端**：邮箱注册/登录后即可在应用商店中部署本地大模型。

### 其他安装方式

有关手动安装、配置选项，请参考帮助手册。macOS / Linux 客户端即将上线。

## 新手入门

1. 下载模型

2. 下载镜像

3. 部署应用

4. 使用模型

## 平台支持

- [x] Windows（天枢模坊客户端）
- [x] Linux
- [ ] macOS（即将上线）

## 加速框架支持

- [x] NVIDIA CUDA ([Compute Capability](https://developer.nvidia.com/cuda-gpus) 6.0 以上)

我们计划在未来的版本中支持以下加速框架：

- [ ] AMD ROCm
- [ ] 海光 DCU
- [ ] 昇腾 CANN
- [ ] Intel oneAPI
- [ ] Apple Metal (M 系列芯片)

## 模型支持

支持从以下来源部署模型：

1. [Hugging Face](https://huggingface.co/)（国内自动走 hf-mirror 镜像加速）

2. [ModelScope](https://modelscope.cn/)

3. 本地文件路径

### 示例模型

| **类别**               | **模型**                                                                                                                                                                                                                                                                                                                                         |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **大语言模型（LLM）**  | [Qwen](https://huggingface.co/models?search=Qwen/Qwen), [LLaMA](https://huggingface.co/meta-llama), [Mistral](https://huggingface.co/mistralai), [Deepseek](https://huggingface.co/models?search=deepseek-ai/deepseek), [Phi](https://huggingface.co/models?search=microsoft/phi), [Yi](https://huggingface.co/models?search=01-ai/Yi)           |
| **多模态模型（VLM）**  | [Llama3.2-Vision](https://huggingface.co/models?pipeline_tag=image-text-to-text&search=llama3.2), [Pixtral](https://huggingface.co/models?search=pixtral) , [Qwen2-VL](https://huggingface.co/models?search=Qwen/Qwen2-VL), [LLaVA](https://huggingface.co/models?search=llava), [InternVL2.5](https://huggingface.co/models?search=internvl2_5) |
| **Diffusion 扩散模型** | [Stable Diffusion](https://huggingface.co/models?search=stable-diffusion), [FLUX](https://huggingface.co/models?search=flux)                                                                                                                                                                                                                     |
| **语音模型**           | [Whisper](https://huggingface.co/models?search=Systran/faster) (speech-to-text), [CosyVoice](https://huggingface.co/models?search=FunAudioLLM/CosyVoice) (text-to-speech)                                                                                                                                                                        |

## OpenAI 兼容 API

`/v1-openai` 路径提供以下 OpenAI 兼容 API：

- [x] [List Models](https://platform.openai.com/docs/api-reference/models/list)
- [x] [Create Completion](https://platform.openai.com/docs/api-reference/completions/create)
- [x] [Create Chat Completion](https://platform.openai.com/docs/api-reference/chat/create)
- [x] [Create Embeddings](https://platform.openai.com/docs/api-reference/embeddings/create)
- [x] [Create Image](https://platform.openai.com/docs/api-reference/images/create)
- [x] [Create Image Edit](https://platform.openai.com/docs/api-reference/images/createEdit)
- [x] [Create Speech](https://platform.openai.com/docs/api-reference/audio/createSpeech)
- [x] [Create Transcription](https://platform.openai.com/docs/api-reference/audio/createTranscription)

例如，你可以使用官方的 [OpenAI Python API 库](https://github.com/openai/openai-python)来调用 API：

```python
from openai import OpenAI
client = OpenAI(base_url="http://myserver/v1-openai", api_key="myapikey")

completion = client.chat.completions.create(
  model="llama3.2",
  messages=[
    {"role": "system", "content": "You are a helpful assistant."},
    {"role": "user", "content": "Hello!"}
  ]
)

print(completion.choices[0].message)
```

用户可以在 UI 中生成自己的 API 密钥。

## 文档

完整文档请参见官网：[bartplanet.ai](https://bartplanet.ai/)（项目介绍、技术白皮书、商业 BP 等）。

## 参与贡献

欢迎参与贡献代码：https://github.com/BartPlanet/PivotAIOS

## 加入社区

巴特星球永远为相信「智能平权、共创 Token 经济体」的伙伴敞开。欢迎加入社区群：

- **社区秘书（微信）**：byteverse888

---

© 巴特星球 · AI 价值网络 | 智能平权 · 共创 Token 经济体
