# 更新记录 / Changelog

[简体中文](#简体中文) · [English](#english)

## 简体中文

### v0.1.0-beta.8 — 2026-11-21

按 Cineon26 0.5.0（129）更新，并重新整理 Skill 的入口与操作指引。

- 按导入、继续处理、恢复项目或接续导出进入相应步骤，减少重复检查和不必要的重新校色。
- 更新统一导入、扫描 TIFF、分帧与合回流程，区分继承结果、区域复核和已完成处理。
- 默认逐张自动校色；按需使用参数复制、Color Balance 与中性参考，保留场景色调和已有编辑。
- 更新画框、裁切、快照与缓存恢复说明，按实际提示处理原片访问、ICC 和可恢复错误。
- 修正 HEIC 保留 HDR 的说明：每张照片按当前 SDR／HDR 模式导出，混合选区逐张核对。
- 精简记录与文件核验要求，不再强制普通处理反复计算全部原片哈希，也不默认生成最大体积成片。

仍先保存项目交给你检查、打分，收到导出要求后再继续。

### v0.1.0-beta.7 — 2026-11-15

按 Cineon26 0.5.0（126）更新操作说明，涵盖自 120 以来的累计变化。

- 改为整图导入后按需分帧，说明已校色子帧的编辑继承、逐帧 Auto、合回整条及三色分帧的限制。
- 补充未收录胶卷、其他画幅和项目内名称编辑，不把名称当作画框尺寸。
- 区分 SDR／HDR 的独立影调与共用 Color Balance，说明 HDR 直方图、观看背景及独立 HDR 导出。
- 增加白底导出的版式、尺寸与上次设置检查，完善网络目录访问恢复。
- 更新画框快捷键、分帧集合选择、快照与缓存恢复，保留已有项目编辑。

流程仍为：导入和初步处理，保存后交给你检查打分，收到要求后再导出。

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

### v0.1.0-beta.8 — 2026-11-21

Update the Skill for Cineon26 0.5.0 (129) and reorganize its entry point and operating guidance.

- Start at the relevant step for importing, continuing edits, recovering a project, or resuming export, avoiding redundant checks and unnecessary Auto Color passes.
- Update unified import, scanner TIFF, splitting, and joining guidance; distinguish inherited results, geometry review, and completed processing.
- Use independent Auto Color by default, with parameter reuse, Color Balance, and neutral references when appropriate, preserving scene lighting and existing edits.
- Refresh frame, crop, snapshot, and cache-recovery guidance, following actionable messages for source access, ICC profiles, and recoverable errors.
- Correct Preserve HDR guidance: HEIC uses each photo's current SDR/HDR mode, including mixed selections.
- Simplify tracking and file verification. Routine work no longer requires repeated full-source hashing or defaults to the largest export files.

Projects still stop for your review and ratings after saving. Export begins only when requested.

### v0.1.0-beta.7 — 2026-11-15

Update operating guidance for Cineon26 0.5.0 (126), covering the cumulative changes since Build 120.

- Import complete images and split as needed, with guidance for inherited edits, per-frame Auto, joining strips, and RGB split limitations.
- Add Unlisted Film, Other Frame Format, and project-local names without treating names as frame dimensions.
- Distinguish separate SDR/HDR tonal edits from shared Color Balance, and explain HDR histograms, viewing backgrounds, and independent HDR export.
- Add white-background export layouts, final canvas dimensions, remembered settings, and network-folder access recovery.
- Update geometry shortcuts, split-collection selection, snapshots, and cache recovery while preserving project edits.

The workflow remains: import and prepare, save for your review and ratings, then export only when requested.

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
