# Entropy OS（熵 OS）

[English](#english)

Entropy OS 是基于 Debian 13（trixie）构建的桌面操作系统，自带本机运行的 AI 助手。

这个仓库只放说明、截图和链接，**不包含 Entropy OS 的源代码**。系统下载、开源组件的源码和用户协议都在 [lyrasama.com/os](https://lyrasama.com/os/)。

![Entropy OS 安装程序](screenshots/installer.png)

## 核心特点

- **本地优先**：AI 助手默认使用本机模型，你的文件、屏幕内容和语音都在本机处理。云端模型默认关闭，要你单独同意才会用，并会先列出会发送哪些内容。
- **有 AI 更好，没有 AI 也能用**：没有独立显卡、或者还没下载模型时，系统、软件和文件操作都照常可用，助手功能等有了模型再打开。
- **不收集个人信息**：系统本身没有遥测代码，不收集、也不上传使用数据。
- **执行前必须确认**：删除、覆盖、发送、安装等可能造成不可逆影响的操作，助手都要先得到你的确认。

![首次设置：隐私](screenshots/first-boot-privacy.png)

## 版本

| | 个人版 | 企业版 |
|---|---|---|
| 适合 | 个人在自己的电脑上使用 | 公司、学校等单位统一部署 |
| 媒体格式 | 可以播放 AAC-LC 音频和 AMR 语音；H.264 可在设置里选择从 Cisco 下载 OpenH264 | 不含专利编解码器，由单位按自己持有的许可补齐 |
| 全盘加密 | 安装时可选 | 默认开启 |

## 系统要求

- UEFI 启动（不支持传统 BIOS），可以开着安全启动安装
- 64 位 x86（amd64）处理器，4 核以上
- 内存最少 8 GB，推荐 16 GB 以上
- 推荐 Intel 或 AMD 显卡；要用本机 AI 模型的完整功能，推荐 6–8 GB 以上显存
- 8 GB 以上的 U 盘，用来制作安装盘

## 下载

请到 **[lyrasama.com/os](https://lyrasama.com/os/)** 下载。下载页上有：

- ISO 文件；
- SHA256 校验值、签名文件和签名公钥的指纹；
- 中文的 U 盘制作和校验步骤。

请只从这个地址下载，并在安装前核对校验值和签名。

## 已知问题

- 新款 NVIDIA 显卡的支持还没有验证过。系统默认用开源的 nouveau 驱动，不预装 NVIDIA 专有驱动。
- Microsoft UEFI CA 2011 证书已于 2026 年 6 月到期。镜像用的是同时带新旧两种签名的 shim，一般不受影响；很老的电脑开着安全启动无法启动时，请先更新主板固件。

## 开源组件

Entropy OS 包含许多开源软件，例如 Linux 内核、桌面环境、系统工具和安装器。它们按各自的许可提供：

- 许可证全文和版权声明：[lyrasama.com/os/notice](https://lyrasama.com/os/notice)
- GPL、LGPL 等许可要求的对应源码：[lyrasama.com/os/source/](https://lyrasama.com/os/source/)，每个版本至少保留三年

## 许可

- Entropy OS 本身是专有软件，按[用户协议](https://lyrasama.com/os/eula)提供，同时包含按各自许可提供的开源组件。用户协议不限制开源许可给你的任何权利。
- 本仓库的说明文字和截图：[许可待定]
- 著作权人：weisen

## 反馈

这个仓库**不受理 issue 和 pull request**。问题和建议请通过网站的匿名反馈提交：[lyrasama.com/feedback](https://lyrasama.com/feedback)。反馈是匿名的，请不要填写个人信息。

## 声明

Entropy OS 不是 Debian 项目的产品，未获 Debian 项目或 SPI 的赞助、关联或认可。Debian 是 Software in the Public Interest, Inc. 的注册商标。

---

## English

Entropy OS is a desktop operating system built on Debian 13 (trixie), with an AI assistant that runs on your own computer.

This repository contains only this description, screenshots and links. **It does not contain the source code of Entropy OS.** Downloads, the source code of the open-source components and the license agreement are at [lyrasama.com/os](https://lyrasama.com/os/). The download page is in Chinese.

### Highlights

- **Local first.** The assistant uses a model on your computer by default; your files, screen and voice are processed locally. Cloud models are off by default and are used only after you agree, with a list of what would be sent.
- **Better with AI, fine without it.** Without a graphics card or a model, the system, apps and files work as usual; the assistant switches on once a model is available.
- **No personal data collected.** The system has no telemetry code and sends no usage data.
- **Confirmation before action.** Deleting, overwriting, sending, installing and other actions that are hard to undo always ask you first.

### Editions

- **Personal:** for your own computer. Plays AAC-LC audio and AMR speech; H.264 via Cisco's OpenH264, downloaded only if you choose to. Full-disk encryption is optional.
- **Enterprise:** for organizations. No patent-encumbered codecs; organizations add their own licensed ones. Full-disk encryption is on by default.

### System requirements

- UEFI boot (legacy BIOS is not supported); Secure Boot can stay on
- 64-bit x86 (amd64) processor, 4 cores or more
- 8 GB of memory at least, 16 GB or more recommended
- Intel or AMD graphics recommended; 6–8 GB of video memory or more for the full local AI features
- A USB stick of 8 GB or more for the installer

### Known issues

- Support for recent NVIDIA graphics cards has not been verified. The open-source nouveau driver is used by default; the proprietary NVIDIA driver is not preinstalled.
- The Microsoft UEFI CA 2011 certificate expired in June 2026. The image uses a shim signed with both the old and the new certificate, so most computers are not affected. If a very old computer will not boot with Secure Boot on, update its firmware first.

### Open-source components

- Licenses and copyright notices: [lyrasama.com/os/notice](https://lyrasama.com/os/notice)
- Corresponding source code required by the GPL, LGPL and similar licenses: [lyrasama.com/os/source/](https://lyrasama.com/os/source/), kept for at least three years per release

### License

- Entropy OS itself is proprietary software, provided under its [license agreement](https://lyrasama.com/os/eula), and includes open-source components under their own licenses. The agreement does not limit any rights those open-source licenses give you.
- Text and screenshots in this repository: [license to be decided]
- Copyright holder: weisen

### Feedback

This repository **does not accept issues or pull requests**. Please use the anonymous feedback form on the website: [lyrasama.com/feedback](https://lyrasama.com/en/feedback). It is anonymous, so please don't include personal details.

### Notice

Entropy OS is not a product of the Debian Project and is not sponsored, affiliated with or endorsed by the Debian Project or SPI. Debian is a registered trademark of Software in the Public Interest, Inc.
