# Cineon26 Skills

让 Codex 操作 Cineon26，完成胶片导入、初步校色、画框检查与修复；你检查、打分之后，再按你的要求导出。

**当前版本：v0.1.0-beta.1（公开测试版）**

这是操作 macOS App 的 Skill，需要你已安装并可使用 Cineon26。仓库只包含操作说明和 Skill 元数据，不包含 Cineon26 应用、算法实现、源码、照片、工程、处理缓存或 ICC 文件。

## 使用条件

- macOS 和可用的 Cineon26，具备相应编辑与导出权限。
- Codex 桌面环境中有支持原生 macOS App 的 Computer Use 工具，并已完成所需系统授权。仅有终端或浏览器操作能力不足以运行本 Skill。
- 能访问你指定的原片目录和输出目录。

Skill 不会安装 Cineon26，也不会自行获得鼠标、屏幕或账户权限。界面操作能力取决于你使用的 Codex 环境；安装 Skill 不等于这些能力已启用。

## 安装

推荐在 Codex 中输入：

```text
用 $skill-installer 安装 https://github.com/kehanXue/Cineon26-Skills/tree/v0.1.0-beta.1/skills/cineon26-process
```

也可以从 [Releases](https://github.com/kehanXue/Cineon26-Skills/releases/tag/v0.1.0-beta.1) 下载 GitHub 提供的 **Source code (zip)**，解压后把 `skills/cineon26-process` 整个文件夹放入 `~/.agents/skills/`。这个 ZIP 只包含本仓库的 Skill 和说明文件。不要同时在多个技能目录保留同名副本。安装后在新一轮对话中使用；如果没有出现，重启 Codex。

Skill 目录应包含 `SKILL.md`、`agents/openai.yaml` 和 `references/`。安装机制见 [OpenAI 官方说明](https://learn.chatgpt.com/docs/build-skills)。

## 使用示例

### 导入并初步处理

```text
用 $cineon26-process 处理 ~/Pictures/FilmScans/旅行这一卷。
里面是 Portra 160，120 的 6×6。全部导入、初步校色，画框不对就修，保存后叫我检查打分，先不导出。
```

文件夹名字不需要固定格式。Skill 会结合名称、上下文和你提供的信息判断胶卷及画幅；仍不明确时按文件夹询问。你可以直接给出目录，不必先把所有设置整理成表格。

### 检查打分后导出

```text
我已经检查并打分。把所有有星标的照片，以及 4×5 分组下的全部照片导出到 ~/Downloads/Cineon26-Exports。
使用原始尺寸、16-bit TIFF、ProPhoto RGB。
```

Skill 会读取项目当前评分、编辑和裁切，合并范围并避免重复导出。未明确要求导出时，会停在“可以开始检查、打分”的阶段。

### 已知处理行为

- 相机 RAW 出现明显偏色时，可以启用 Color Balance 并复查；保留场景本来的光线和色调。
- 对明确的画框或负片片基错误，通过 App 界面修复后重新处理。
- 经看图确认只有片基、没有实际画面的片段，跳过细致校色，取舍留给你。
- 3F 扫描 `.fff` 与相机 `.3fr` 分开识别。需要的扫描 ICC 缺失时，从 [Flextight-X5-ICC](https://github.com/kehanXue/Flextight-X5-ICC) 下载并通过 App 设置导入；ICC 不随本仓库分发。

## 已验证范围

在 Cineon26 0.5.0 的 build 95–97 上完成过真实 App 操作：

- 完整 3F 批次：60 个原文件、161 帧，覆盖多种彩色负片和反转片，以及 XPan、135、4×5。
- 用户检查打分后，按“星标或 4×5”导出 15 张 TIFF；文件核验通过，用户已确认导出结果。
- 相机 RAW：4 张 NEF，覆盖 Portra 160、Ektar 100、Vision3 500T 5219、Provia 100F，以及 120 6×6、XPan；包括修框和 Color Balance 操作。
- 遇到导出缓存缺失时，通过 App 的 100% 预览恢复后重试成功，保留了用户编辑和评分。

这证明上述样本的操作流程跑通。其他 RAW 容器、RGB 三色合成、平场参考、缺失/错误 ICC 的完整恢复、导出中断、同名文件和裁切区域导出仍需更多实测；不承诺所有输入都能自动成功。已验证版本以本节为准，新版界面以实际控件为准。

## 反馈

请通过 [Issues](https://github.com/kehanXue/Cineon26-Skills/issues) 说明 Cineon26 版本、输入类型、画幅、操作步骤和可见错误。提交前检查截图和文字，避免公开私人照片、完整本机路径或未经整理的项目日志。

Cineon26 应用自身的版权和许可独立适用；公开这些操作说明不授予其源码或算法的使用权。此仓库尚未指定开源许可证。
