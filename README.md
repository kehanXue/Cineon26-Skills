# Cineon26 Skills

[English](#english) · [简体中文](#简体中文)

## English

Let Codex operate Cineon26 to import film captures, prepare initial color, and check or repair frame selections. When the project is ready, you review and rate the photos, then tell Codex what to export and which settings to use.

### Requirements

- Cineon26 installed and available on your Mac. These instructions follow 0.5.0 (114); controls may differ in other builds.
- A Codex environment with Computer Use support for native macOS apps and the necessary system permissions.
- Access to your source and export folders.

### Install

In Codex, enter:

```text
Use $skill-installer to install https://github.com/kehanXue/Cineon26-Skills/tree/v0.1.0-beta.3/skills/cineon26-process
```

Or download **Source code (zip)** from [Releases](https://github.com/kehanXue/Cineon26-Skills/releases/tag/v0.1.0-beta.3), extract it, and copy the `skills/cineon26-process` folder into `~/.agents/skills/`. Keep only one installed copy of the Skill. If it does not appear in Codex, restart the app.

### Use

**1. Import and prepare**

Give Codex a folder and any film information you know:

```text
Use $cineon26-process to process ~/Pictures/FilmScans/Weekend.
These are Portra 160, shot on 120 film in 6×6 format.
Import everything, prepare initial color, and fix incorrect frame selections.
Save the project and let me know when I can review and rate the photos. Do not export yet.
```

Folder names do not need a fixed format. The Skill uses the names and your description to understand the film stock and frame format, and asks about individual folders when information is missing or ambiguous.

It works with camera RAW captures, compatible scanner Linear DNG files, and Hasselblad 3F (`.fff`) scans. Single-frame files import directly; when a source image contains several frames or film strips, Codex reviews the strip and frame counts and adjusts the dividers before processing. It checks the automatic-processing option to avoid submitting the same batch twice. For RAW files with a color cast, it can enable Color Balance while preserving the scene's lighting. Segments containing only film base are left for you to discard or keep, without detailed color adjustment. For 3F scans, missing ICC profiles can be downloaded from [Flextight-X5-ICC](https://github.com/kehanXue/Flextight-X5-ICC) and imported into Cineon26.

**2. Review, rate, then export**

Check the project in Cineon26, make any edits, and rate the photos. Then give Codex your export instructions:

```text
I have finished reviewing and rating the photos.
Export every starred photo and all photos in the 4×5 group to ~/Downloads/Cineon26-Exports.
Use original dimensions, 16-bit TIFF, and ProPhoto RGB.
```

The Skill uses the project's current ratings, edits, and crop settings, and avoids exporting the same photo twice when selections overlap. It exports only when you ask.

For HDR delivery, request HEIC (HDR) with Preserve HDR; the selected photos must have HDR Mode enabled. TIFF, PNG, and JPG export SDR in this build. State whether you want the current crop or the full image.

If a project needs recovery, Codex follows the app's guidance for source access, missing files, ICC profiles, or cached results while preserving your edits and ratings. Keep your originals: a project file does not contain them.

### Feedback

Report problems or suggest improvements in [Issues](https://github.com/kehanXue/Cineon26-Skills/issues). Include your Cineon26 version and the steps leading to the problem; check screenshots for private information before posting.

This repository contains Skill instructions and metadata. Cineon26 is distributed separately; its application code, algorithms, and user photos are not included. Cineon26's own terms apply independently. This repository currently has no open-source license.

## 简体中文

让 Codex 操作 Cineon26，完成胶片导入、初步校色、画框检查与修复。项目准备好后，由你检查、打分，再告诉 Codex 导出哪些照片、使用什么设置。

### 使用条件

- Mac 上已安装并可使用 Cineon26。本版说明对应 0.5.0（114），其他构建的控件可能不同。
- Codex 环境具备原生 macOS App 的 Computer Use 能力，并已获得所需系统权限。
- 能访问你的原片目录和导出目录。

### 安装

在 Codex 中输入：

```text
用 $skill-installer 安装 https://github.com/kehanXue/Cineon26-Skills/tree/v0.1.0-beta.3/skills/cineon26-process
```

也可以从 [Releases](https://github.com/kehanXue/Cineon26-Skills/releases/tag/v0.1.0-beta.3) 下载 **Source code (zip)**，解压后把 `skills/cineon26-process` 文件夹放入 `~/.agents/skills/`。只保留一份已安装的同名 Skill；如果 Codex 中没有出现，重启应用。

### 使用

**1. 导入并初步处理**

把文件夹交给 Codex，附上你知道的胶卷信息即可：

```text
用 $cineon26-process 处理 ~/Pictures/FilmScans/旅行这一卷。
里面是 Portra 160，120 的 6×6。
全部导入、初步校色，画框不对就修。
保存项目后叫我检查打分，先不导出。
```

文件夹名字不需要固定格式。Skill 会结合名称和你的描述理解胶卷型号、画幅；信息缺失或有歧义时，再按文件夹询问。

可以处理相机翻拍 RAW、兼容扫描仪的线性 DNG，以及哈苏 3F（`.fff`）扫描文件。单帧文件直接导入；一张原图含有多张画面或多条胶卷时，Codex 会先复核条数、帧数与分隔线，再处理，并检查自动处理开关，避免重复提交同一批校色。RAW 有偏色时，可以启用 Color Balance，同时保留场景本来的光线和色调。只有片基、没有实际画面的片段不做细致校色，取舍留给你。3F 所需的 ICC 缺失时，可以从 [Flextight-X5-ICC](https://github.com/kehanXue/Flextight-X5-ICC) 下载并导入 Cineon26。

**2. 检查、打分，再导出**

在 Cineon26 中检查项目，完成需要的编辑和评分，再告诉 Codex 怎么导出：

```text
我已经检查并打分。
把所有有星标的照片，以及 4×5 分组下的全部照片导出到 ~/Downloads/Cineon26-Exports。
使用原始尺寸、16-bit TIFF、ProPhoto RGB。
```

Skill 会使用项目当前的评分、编辑和裁切设置，合并选择范围，避免重复导出。只有在你明确要求后才会导出。

需要 HDR 成片时，指定 HEIC（HDR）并保留 HDR；目标照片需已开启 HDR 模式。本构建中的 TIFF、PNG、JPG 导出 SDR。请说明使用当前裁切还是完整画面。

项目需要恢复时，Codex 会按 App 提示处理原片权限、缺失文件、ICC 或缓存问题，保留已有编辑和评分。请保管原片，项目文件不包含它们。

### 反馈

欢迎通过 [Issues](https://github.com/kehanXue/Cineon26-Skills/issues) 反馈问题或建议。请注明 Cineon26 版本和出现问题的操作步骤；提交截图前检查是否含有私人信息。

本仓库只包含 Skill 操作说明和元数据。Cineon26 应用单独提供，不包含在这里，其源码、算法和用户照片也不随本仓库分发。Cineon26 自身的许可独立适用；本仓库尚未指定开源许可证。
