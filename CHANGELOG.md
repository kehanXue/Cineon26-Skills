# 更新记录 / Changelog

[简体中文](#简体中文) · [English](#english)

## 简体中文

### v0.1.0-beta.6 — 2026-11-01

双语说明统一为简体中文在前、英文在后。包含 beta.5 的 Cineon26 120 处理与恢复操作更新。

### v0.1.0-beta.5 — 2026-11-01

完善 Cineon26 0.5.0（120）的处理与恢复操作说明。

- 明确负片与反转片 ICC 适用于彩色 3F；黑白 3F 不需要这两项 profile。
- 补充平场参考、翻拍质量、镜头校正，以及三色和独立白光照片的操作。
- 说明基础与后期控件的作用范围、中性取样、图像对比及保持白色齿孔。
- 按输入类型核对控件与快照的可用性，通过实际提供的操作恢复已有编辑。
- 导出前核对评分、筛选条件、实际选区及重叠分组，避免遗漏或重复。
- 区分找回原片和授予访问权限，不接受同名但内容不匹配的文件。

导入和初步处理后仍交给你检查；收到导出要求后，才按最新编辑继续。

### v0.1.0-beta.4 — 2026-11-01

按 Cineon26 0.5.0（120）更新操作说明，涵盖自 Build 114 对应 Skill 发布以来的变化。

- 补充黑白负片选择与明暗调整，以及兼容的 16-bit 线性 RGB TIFF 输入。
- 说明彩色 3F 的独立 Color Balance 和新版 ICC 设置。
- 更新分隔线复核、画框自由拖动、检测缩放比例，以及保留裁切时查看完整图片的操作。
- 跟进自由比例裁切默认值，以及进出裁切工具时保留图像显示尺度的行为。
- 处理旧画框、原片权限、项目重开和缓存恢复，避免用重新 Auto 覆盖已有编辑。
- 补充黑白 HDR、屏幕显示受限提示和当前 SDR／HDR 导出选项。

流程仍为：导入并初步处理，保存后交给你检查打分，收到要求后再导出。

### v0.1.0-beta.3 — 2026-10-22

按 Cineon26 0.5.0（114）更新操作说明，涵盖自上次 Skill 发布以来的累计变化。

- 统一 RAW、兼容扫描仪线性 DNG、3F 的单帧与多画面导入，复核胶卷条数和分帧。
- 检查导入或确认分帧后的自动处理选项，避免重复自动校色。
- 更新画框、缩放平移、重置识别区域与裁切操作。
- 补充批量 Color Balance 和快照使用，保留每张照片的独立编辑。
- 区分原片权限、文件缺失、ICC 问题和缓存恢复。
- 补充 SDR 格式、Display P3 和 HEIC HDR 导出，使用当前评分与裁切。

默认仍在保存项目后交给你检查打分；收到明确要求后才导出。

### v0.1.0-beta.2 — 2026-10-15

- 补充英文和简体中文说明。
- 精简 README 和 Release 说明，聚焦安装、检查与导出。
- Skill 行为保持不变。

### v0.1.0-beta.1 — 2026-10-15

首次公开测试版。

- 导入胶片、初步校色、检查画框，并处理常见界面错误。
- 结合文件夹名字和对话理解胶卷型号、画幅。
- 保存项目交给用户检查打分；收到要求后，按项目当前编辑导出。
- 提供 RAW Color Balance、3F 分帧、ICC 配置和导出缓存缺失时的操作提示。

## English

### v0.1.0-beta.6 — 2026-11-01

Present Simplified Chinese before English throughout the bilingual documentation. Includes the Cineon26 120 processing and recovery updates from beta.5.

### v0.1.0-beta.5 — 2026-11-01

Refine the processing and recovery instructions for Cineon26 0.5.0 (120).

- Clarify that the negative and reversal ICC profiles are for color 3F scans; black-and-white 3F scans do not require them.
- Expand guidance for flat-field references, capture quality, lens correction, and separate RGB and white-light photos.
- Explain the scope of Basic and Post-processing controls, neutral sampling, image comparison, and white perforations.
- Check control and snapshot availability for each input type, and restore saved edits only through the available app controls.
- Check ratings, filters, actual photo selection, and overlapping groups before export.
- Distinguish locating an original from granting access, and reject a same-named file when its content does not match.

Import and initial preparation still stop for your review. Export uses your latest edits only after you request it.

### v0.1.0-beta.4 — 2026-11-01

Update operating guidance for Cineon26 0.5.0 (120), covering the changes since the Build 114 Skill release.

- Add black-and-white negative selection and tonal controls, plus compatible 16-bit linear RGB TIFF input.
- Explain independent Color Balance for color 3F scans and the updated ICC settings.
- Update strip-divider review, free-aspect geometry dragging, frame-detection scale, and full-image inspection with a saved crop.
- Follow free-aspect crop defaults and preserve image scale when entering or leaving the crop tool.
- Handle old geometry, source access, project reopening, and cache recovery without replacing saved edits with a new Auto pass.
- Include black-and-white HDR, limited-display guidance, and current SDR/HDR export options.

The workflow remains: import and prepare, save for your review and ratings, then export only when requested.

### v0.1.0-beta.3 — 2026-10-22

Update operating guidance for Cineon26 0.5.0 (114), including changes accumulated since the previous Skill release.

- Use unified single-frame and multi-frame import for RAW, compatible scanner Linear DNG, and 3F, with strip and frame review.
- Check automatic processing after import or split confirmation and avoid duplicate Auto Color work.
- Follow the updated frame controls, zoom and pan, geometry reset, and crop behavior.
- Add batch Color Balance and snapshot guidance while preserving individual edits.
- Distinguish source access, missing files, ICC problems, and cache recovery.
- Document SDR formats, Display P3, and HEIC HDR export using current ratings and crops.

The review-and-rate handoff remains the default; export still requires your request.

### v0.1.0-beta.2 — 2026-10-15

- Add English and Simplified Chinese documentation.
- Simplify the README and release notes around installation, review, and export.
- No changes to Skill behavior.

### v0.1.0-beta.1 — 2026-10-15

First public beta.

- Import film captures, prepare initial color, check frames, and recover from common GUI errors.
- Understand film stock and frame format from folder names and conversation.
- Save the project for review and rating; export only when requested, using the current project edits.
- Include guidance for RAW Color Balance, 3F frame splitting, ICC setup, and missing export caches.
