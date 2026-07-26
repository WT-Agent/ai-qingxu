<div align="center">

# [网腾无限AI - 情绪收纳与心理疗愈]

**[一个支持功德木鱼打卡敲击与五种特色疗愈流派的情绪分析与认知重塑工具，具备深色玻璃拟态自适应交互与微信端 H5 体验]**

[Vue 3] · [TypeScript] · [Vite] · [Vanilla CSS] · [开源协议 MIT]

[![GitHub stars](https://img.shields.io/github/stars/WT-Agent/ai-qingxu?style=social)](https://github.com/WT-Agent/ai-qingxu)
[![GitHub license](https://img.shields.io/github/license/WT-Agent/ai-qingxu)](https://github.com/WT-Agent/ai-qingxu/blob/main/LICENSE)

[在线演示](#在线演示) · [快速启动](#快速启动) · [参与贡献](#参与贡献) · [支持一下](#支持一下)

</div>

## 关于我们

团队成员均来自 C9 等顶尖学府，在字节、腾讯、阿里的工程师组成，全职创业研发开源 AI 应用产品，让所有人感受 AI 的魅力。

本项目旨在为面临压力、感到焦虑、自我怀疑或深陷人际纠结的用户提供高品质的情绪倾听、认知重塑与落地自愈指导。用户只需输入烦恼场景与情绪细节，AI 即可根据多维科学度看板自动输出情感共鸣倾听、思维偏差剖析、落地疗愈微行动以及治愈手账悄悄话。页面内置了支持物理发音的互动“功德木鱼”印章，协助用户在情绪梳理中快速建立认知秩序与行动落地。

**我们不搞概念，不卖课，只写能跑起来的代码。**

欢迎 Star、Fork、提 Issue，一起让这个项目变得更好用。

核心特性：
- **极简自适应交互**：提供毛玻璃质感的深色玻璃拟态自适应 Web 界面，高度适配移动端 H5 微信浏览器与 PC 体验。
- **功德木鱼印章 (Muyu Stamp)**：基于前端 Web Audio API 动态合成空灵清脆的木鱼声效，点击即可累积功德/减少焦虑，并伴随渐隐上升动画。
- **五大心理疗愈流派**：
  - **心理咨询师**：极致专业、客观温柔，多用心理学规范词汇，提供CBT分析。
  - **毒舌冷幽默**：一针见血拆穿借口，以戏谑消解沉重，让人破涕为笑。
  - **温暖疗愈系**：笔触极其温柔，像冬日里的热可可，提供全面的安抚与滋养。
  - **理性逻辑流**：结构极为清晰，将纠结情感拆解为具象问题与解决方案步骤。
  - **赛博木鱼敲击**：禅意十足，引导用户放下内耗执念，四大皆空。
- **AI 疗愈质量看板**：自动提取 AI 回复中的共识数据，以简洁的单轨进度条在前端直观展示共情指数、认知重构度、自愈指数、痛点拆解度及焦虑缓解度。
- **演示案例与分享卡片**：内置 30 条不同类型的情绪自愈与心理疗愈演示样例，并支持一键卡片化截图分享。
- **一键零成本部署**：纯前端静态网页结构，支持零成本部署于 Vercel、GitHub Pages 或 CDN/OSS 静态托管服务。
- **安全开发代理**：本地开发支持使用个人 API 密钥发起代理请求，密钥由 Vite 服务器中转，无需担心前端泄露。
- **裂变解锁与留存**：内置微信朋友圈扫码分享拦截与额度重置机制，提升流量转化与留存。

## 快速启动

### 1. 克隆项目
```bash
git clone https://github.com/WT-Agent/ai-qingxu.git
cd ai-qingxu
```

### 2. 安装依赖
项目强制使用 pnpm 作为包管理器：
```bash
pnpm install
```

### 3. 配置本地开发环境变量
复制并修改环境变量配置文件：
```bash
cp .env.example .env
```
根据微应用的功能类型，在 `.env` 中配置您的开发者密钥：
- `DEEPSEEK_API_KEY`: 您的 DeepSeek 开发者 API 密钥（用于文本生成任务）
- `DASHSCOPE_API_KEY`: 您的通义千问/通义万相开发者 API 密钥（用于多模态与生图任务）

### 4. 启动本地开发服务
```bash
pnpm dev
```
启动成功后在浏览器访问控制台输出的地址即可。

### 5. 生产构建打包
```bash
pnpm build
```
打包后生成的 `dist` 目录即为纯静态网页资源，可直接上传部署。

## 脚手架集成说明

本模板由私有总控仓库 `ai.wuxian.xyz` 中的 `@wuxian/cli` 脚手架统一管理，支持以下批量运维操作：

### 初始化或更新单个子项目

```bash
node bin/cli.js ai-qingxu
```

脚手架将自动：
1. 读取子仓库的 `README.md` 首行作为 Prompt 主题。
2. 注入 Vue 3 静态页面结构及标准配置文件。
3. 保留原有的 `.git` 配置与 `README.md`，不覆盖个性化内容。

### 批量同步所有子项目

```bash
node bin/cli.js all
```

将模板 the latest 变更（如 SSO 逻辑、额度控制）一键同步至全部 31 个子项目。

### Agent 配置维护接口

```bash
# 读取子项目配置
node bin/cli.js get ai-qingxu

# 写入/更新配置（支持热更新 prompt、model、title、temperature 等）
node bin/cli.js set ai-qingxu prompt "你是一个结合专业心理咨询师、CBT认知行为治疗专家、诗意疗愈系作家以及冷幽默倾听者的智能情绪收纳顾问..."
node bin/cli.js set ai-qingxu model deepseek-chat
```

## 联系方式

- GitHub Issues: [提交反馈](https://github.com/WT-Agent/ai-qingxu/issues)
- 邮箱: us@wuxian.xyz

## 打赏支持

如果本项目对您有帮助，欢迎请作者喝杯咖啡。您的支持是持续维护与更新的动力。

<div align="center">

**微信支付** | **支付宝**
:---:|:---:
<img src="./asset/tenpay.png" width="200" alt="微信支付"> | <img src="./asset/alipay.png" width="200" alt="支付宝">

</div>

## 版权与许可

本项目基于 MIT License 开源协议。

Copyright (c) 2026. All rights reserved.
