# dsh-pet-live2d（个人修改版）

给 **DSH**（DeepSeek Harness）Web GUI 用的 Live2D 桌宠插件 —— 一只可以拖动、跟着鼠标转头、
点她会害羞、会跟着会话状态换动作的桌宠。

本仓库是 [A8Chann/dsh-pet-live2d](https://github.com/A8Chann/dsh-pet-live2d) **v3.5.0（MIT）的个人修改版**，
在网页端（`lib/client.js`）上做了一批修复与增强，并附带一只转换好的免费公皮模型。

## 相比上游的改动

- **修复鼠标追踪**：部分构建里 vendor 的视线缓动没有真正落到帧里，头部不跟鼠标。
  现在由插件每帧自己驱动注视（头 ±30°、眼珠、身体轻倾），垂直方向按 Cubism「抬头为正」约定。
- **新增程序化待机微动**：多层非谐波摆动 + 呼吸包络 + 偶发瞥视（每 7–10 秒随机方向看一眼），
  **幅度/速度可在设置面板「待机」卡里调**（0 = 完全静止）；动作播放时自动让位。
- **对话气泡重做**：居中于角色正上方、屏幕边缘自动夹回并把尾巴指向角色、上方放不下时翻到下方；
  渐变纸面 + 弹出/淡出动画。
- **右键面板加回「设置」页签**（部分版本里 DSH 设置页入口不可达）。
- **气泡锚点改用实时头部网格**：修正缓存几何导致气泡飘出屏幕的问题。
- **表情停留时长 12s → 4s**（摸鱼表情、手动表情、摸摸反应一致）。

完整明细见 [MODIFICATIONS.md](./MODIFICATIONS.md)。

## 附带的模型

- `pets/dafish/` — **不托管模型文件**。大肥鱼（DeepSeek-chan）为免费公开配布的模型，
  请到 **B 站搜索「神宫凉子」进入作者主页**获取；原画及拆分 **神宫凉子**，Live2D 建模
  **霓虹猫_NeonNeko**。署名与须知见 [CREDITS.md](./CREDITS.md)，转换方法见
  [pets/dafish/README.md](./pets/dafish/README.md)。
- `pets/ds-whale-girl/` — 上游自带示例宠物（随 MIT 包分发）。

## 安装

1. 把本仓库放进 DSH 的 profile 依赖目录：

   ```bash
   dsh plugin --profile web add <本仓库地址>   # 或手动解压到
   # ~/.dsh/profiles/web/node_modules/dsh-pet-live2d
   ```

2. 把宠物拷进宠物目录：

   ```bash
   cp -r pets/* ~/.dsh/pets/
   ```

3. 刷新 DSH 页面 / 重启 `dsh web`。

## 设置在哪

- 宠物**右键面板 → 设置**（手感 / 待机 / 显示位置 / 会话提示音 / 会话相位 / 摸鱼 / 互动 / 气泡）
- 部分版本也挂在 DSH 设置页的「桌宠」一节（与右键面板共用同一份设置存储）

## 许可

| 内容 | 许可 |
| --- | --- |
| 插件代码 | MIT（Copyright (c) 2026 A8Chann，见 [LICENSE](./LICENSE)） |
| `lib/live2d-vendor.js` | Live2D Cubism 运行时 —— 沿用上游分发方式，使用需遵守 Live2D 的 SDK 许可条款 |
| `pets/dafish/` | 模型作者许可：免费公开配布、个人使用、禁止二次销售（见模型目录内条款） |
| `pets/ds-whale-girl/` | 随上游 MIT 包分发 |

上游说明（安装、动作/表情配置、桌面端等）保留在 [README.upstream.md](./README.upstream.md)。
