# Cineon26 Skills

[简体中文](#简体中文) · [English](#english)

## 简体中文

让 Codex 操作 Cineon26，导入胶片、初步校色、检查和修正画框。项目准备好后，由你检查、打分，再告诉 Codex 导出哪些照片、使用什么设置。

### 使用条件

- Mac 上已安装并可使用 Cineon26。本版说明对应 **0.5.0（129）**，其他构建的控件可能不同。
- Codex 环境具备原生 macOS App 的 Computer Use 能力，并已获得所需系统权限。
- 能访问你的原片、项目和导出目录。

### 安装

在 Codex 中输入：

```text
用 $skill-installer 安装 https://github.com/kehanXue/Cineon26-Skills/tree/v0.1.0-beta.8/skills/cineon26-process
```

也可以从 [Releases](https://github.com/kehanXue/Cineon26-Skills/releases/tag/v0.1.0-beta.8) 下载 Skill ZIP 或 **Source code (zip)**，解压后把 `skills/cineon26-process` 放入 `~/.agents/skills/`。更新时替换已有同名 Skill，只保留一份；如果 Codex 中没有出现，重启应用。

### 导入并初步处理

把文件夹交给 Codex，附上你知道的胶卷信息即可：

```text
用 $cineon26-process 处理 ~/Pictures/FilmScans/旅行这一卷。
里面是 Portra 160，120 的 6×6。
全部导入、初步校色，画框不对就修。
保存项目后叫我检查打分，先不导出。
```

文件夹名字不需要固定格式。Skill 会结合名称和你的描述理解胶卷型号、画幅；信息缺失或有歧义时，再按文件夹询问。菜单中没有的胶卷和画幅可以使用“未收录胶卷”“其他画幅”，保存项目内名称；自定义画幅名称不会自动决定画框比例。

支持相机翻拍 RAW、兼容扫描仪的线性 DNG、兼容的 16-bit RGB TIFF，以及哈苏 3F（`.fff`）扫描文件。彩色负片、反转片和黑白负片分别选择对应胶片。TIFF 需要保留可确认的编码与色彩描述；不要把已经反相、调色的成片当作原始负片导入。JPG、PNG 不是本 Skill 的胶片来源。三色拍摄请提供完整的 R/G/B 序列，以及已有的匹配平场参考。

**先导入完整图像，再按需分帧。** Codex 会检查胶卷条数、画面数和分隔线。未处理的照片在分帧后进行 Auto；已校色的整图分帧后，子帧若已有可用结果，会保留继承的色彩、后期和 SDR／HDR 状态，不重复校色。三色合成等来源若仍提示区域复核，则逐帧检查并按提示处理。需要整条成片时可以合回整条；合回保留各帧色彩，不保留子帧的裁切、旋转和翻转。三色合成同样支持分帧与合回；操作前检查分组与来源是否完整。

默认对每张照片独立自动校色。只有你要求复用已有调整时，才对合适的照片复制参数，并复核结果。

有明显偏色时，Skill 会先核对胶片类型与画框，再使用可用的 Color Balance，保留场景原有光线与色调。黑白负片使用明暗调整；只有片基、没有画面的片段留给你取舍。彩色 3F 缺少所需 ICC 时，可以从 [Flextight-X5-ICC](https://github.com/kehanXue/Flextight-X5-ICC) 下载并导入；黑白 3F 不需要这两项彩色 profile。

### 检查、打分，再导出

在 Cineon26 中检查、编辑和评分，然后告诉 Codex：

```text
我已经检查并打分。
把所有有星标的照片，以及 4×5 分组下的全部照片导出到 ~/Downloads/Cineon26-Exports。
使用原始尺寸、16-bit TIFF、ProPhoto RGB，保留当前裁切，不加白底。
```

Skill 使用项目当前的评分、编辑和裁切，合并重叠范围，只有你明确要求后才导出。

SDR 与 HDR 分别保存影调和后期调整，Color Balance 设置共用。需要 HDR 成片时，指定 **HEIC（HDR）并保留 HDR**，先将目标照片切到 HDR 并检查结果；保留 HDR 会按每张照片当前的 SDR／HDR 模式输出；TIFF、PNG、JPG 输出 SDR。屏幕显示范围的限制不代表文件高光丢失。

需要白边版式时，可要求“保留白色背景”。横片和方片使用 4:3 白底，竖片使用 3:4；照片按画幅相对大小居中。尺寸选项控制包含白边的最终成品，而非内部照片尺寸。请同时说明使用当前裁切还是完整画面。

项目需要恢复时，Codex 会按 App 提示处理原片权限、缺失文件、ICC 或缓存问题，保留编辑与评分。已有预览不等于全分辨率导出已就绪。请保管原片：项目文件不包含它们。

部分 129 构建在重开三色项目后导出 HDR 时，可能提示“已保存的处理参数无法复用”。若按提示重新处理仍失败，请保留工程和已有结果，使用包含此修复的 Cineon26 版本后再导出；更新 Skill 不会更新应用。

### 反馈与分发

欢迎通过 [Issues](https://github.com/kehanXue/Cineon26-Skills/issues) 反馈问题或建议。请注明 Cineon26 版本与操作步骤，发布截图前检查私人信息。

本仓库只包含 Skill 操作说明和元数据。Cineon26 应用单独提供，源码、算法和用户照片不随本仓库分发。Cineon26 自身的许可独立适用；本仓库尚未指定开源许可证。

## English

Let Codex operate Cineon26 to import film captures, prepare initial color, and check or repair frame selections. When the project is ready, you review and rate the photos, then tell Codex what to export and which settings to use.

### Requirements

- Cineon26 installed and available on your Mac. These instructions follow **0.5.0 (129)**; controls may differ in other builds.
- A Codex environment with Computer Use support for native macOS apps and the necessary system permissions.
- Access to your source, project, and export folders.

### Install

In Codex, enter:

```text
Use $skill-installer to install https://github.com/kehanXue/Cineon26-Skills/tree/v0.1.0-beta.8/skills/cineon26-process
```

Or download the Skill ZIP or **Source code (zip)** from [Releases](https://github.com/kehanXue/Cineon26-Skills/releases/tag/v0.1.0-beta.8), extract it, and copy `skills/cineon26-process` into `~/.agents/skills/`. To update, replace your existing copy and keep only one installed Skill with this name. Restart Codex if it does not appear.

### Import and prepare

Give Codex a folder and any film information you know:

```text
Use $cineon26-process to process ~/Pictures/FilmScans/Weekend.
These are Portra 160, shot on 120 film in 6×6 format.
Import everything, prepare initial color, and fix incorrect frame selections.
Save the project and let me know when I can review and rate the photos. Do not export yet.
```

Folder names do not need a fixed format. The Skill uses the names and your description to understand the film stock and frame format, asking about individual folders when information is missing or ambiguous. Stocks and formats absent from the menus can use Unlisted Film and Other Frame Format with project-local names. A custom format name does not set the frame's aspect ratio automatically.

Supported inputs include camera RAW captures, compatible scanner Linear DNG, compatible 16-bit RGB TIFF, and Hasselblad 3F (`.fff`) scans. Color negatives, reversal film, and black-and-white negatives use the corresponding film selection. TIFF input needs verifiable encoding and color information. Do not import an already inverted or color-edited positive as an original negative. JPG and PNG are not film inputs for this Skill. For R/G/B captures, provide the complete exposure sequence and any matching flat-field references.

**Import a complete image first, then split frames as needed.** Codex checks strip counts, frame counts, and dividers. Unprocessed frames need Auto after splitting; frames split from a processed image keep inherited color, Post-processing, and SDR/HDR states when those results are available, without another Auto pass. RGB composites and other sources that still request geometry review are checked and processed frame by frame as prompted. Join Film Strip can restore a complete strip while keeping each frame's color, but not its crop, rotation, or flip. RGB composites also support splitting and joining; check the capture grouping and source completeness before proceeding.

Each photo uses independent Auto Color by default. Parameters are copied only when you ask to reuse an edit, with the destination photos checked afterward.

For visible color casts, the Skill checks the film type and frame selections before using available Color Balance controls, preserving the scene's lighting and color. Black-and-white negatives use tonal controls; segments containing only film base are left for you to keep or discard. Missing ICC profiles for color 3F scans can be downloaded from [Flextight-X5-ICC](https://github.com/kehanXue/Flextight-X5-ICC) and imported into the app. Black-and-white 3F scans do not require these color profiles.

### Review, rate, then export

Review, edit, and rate the project in Cineon26, then tell Codex:

```text
I have finished reviewing and rating the photos.
Export every starred photo and all photos in the 4×5 group to ~/Downloads/Cineon26-Exports.
Use original dimensions, 16-bit TIFF, and ProPhoto RGB. Keep the current crops and do not add a white background.
```

The Skill uses current ratings, edits, and crops, merges overlapping selections, and exports only when you ask.

SDR and HDR retain separate tonal and Post-processing adjustments while sharing Color Balance settings. For HDR delivery, request **HEIC (HDR) with Preserve HDR**. Switch the intended photos to HDR and inspect them first. Preserve HDR exports each photo in its current SDR or HDR mode. TIFF, PNG, and JPG export SDR. A screen's brightness limit does not mean that highlights are missing from the file.

For a white-border layout, request Preserve White Background. Landscape and square photos use a 4:3 canvas; portraits use 3:4. Photos are centered at sizes relative to their film format. The size option controls the final canvas including its border, not the image inside it. Also state whether to use the current crop or the full image.

If a project needs recovery, Codex follows the app's guidance for source access, missing files, ICC profiles, or cached results while preserving edits and ratings. An available preview does not prove that full-resolution export is ready. Keep your originals: a project file does not contain them.

Some 129 builds may reject HDR export after reopening an RGB project because saved processing parameters cannot be reused. If reprocessing as prompted still fails, keep the project and existing results, then retry with a Cineon26 version that includes the fix. Updating the Skill does not update the app.

### Feedback and distribution

Report problems or suggest improvements in [Issues](https://github.com/kehanXue/Cineon26-Skills/issues). Include your Cineon26 version and the steps involved, and check screenshots for private information before posting.

This repository contains Skill instructions and metadata. Cineon26 is distributed separately; its application code, algorithms, and user photos are not included. Cineon26's own terms apply independently. This repository currently has no open-source license.
