# 致谢与皮套原作者声明

## 大肥鱼（DeepSeek-chan）Live2D 模型

本仓库 `pets/dafish/` 中的 Live2D 模型，来自 B 站公开配布的**免费模型**。
**模型版权归原作者所有**，本仓库只是把它转换成了 DSH 宠物包格式（路径 ASCII 化、贴图降采样、
物理参数调整、动作整理等），**不主张任何模型版权**。

| 项目 | 署名 |
| --- | --- |
| 模型名称 | DeepSeek-chan（大肥鱼） |
| 原画及拆分 | **神宫凉子** |
| Live2D 建模 | **霓虹猫_NeonNeko** |
| 模型来源 | 神宫凉子免费配布模型 |
| 获取地址（B 站工房） | [https://gf.bilibili.com/item/detail/1109618072](https://gf.bilibili.com/item/detail/1109618072) |
| 作者 B 站主页 | [https://space.bilibili.com/13737731](https://space.bilibili.com/13737731)（短链 https://b23.tv/8POy29x） |

### 作者的使用须知（摘要）

以下摘自作者随模型发布的《DeepSeek 免费 Live2D 模型使用须知》，
全文见 [`pets/dafish/LICENSE-usage-terms.txt`](./pets/dafish/LICENSE-usage-terms.txt)。

**允许**：
- 个人直播、录播、视频投稿等个人内容创作，以及由此获得的平台收益；
- 调整模型显示、追踪、表情及物理参数；
- 围绕大肥鱼制作表情包、剪辑、动画等衍生内容（发布时请注明模型来源）。

**禁止**：
- ❌ 二次销售（不得把模型作为商品出售或出售使用权）；
- ❌ **擅自重新分发模型文件**——不得将完整模型文件重新上传至网盘、素材网站或其他平台，
  供他人直接下载；如需推荐，请分享作者发布的原始获取页面；
- ❌ 冒充原作者，或故意删除、隐藏原作者信息；
- ❌ 把官方配布模型包装成自己原创的作品；
- ❌ 违法及侵权用途。

**商业合作**：品牌广告、企业宣传等以模型为宣传主体的商业项目，需事先联系作者确认。

### 关于本仓库的合规提示

> ✅ 本仓库**不托管模型文件**（`pets/dafish/` 只保留使用须知与获取方式说明），
> 符合作者「禁止擅自重新分发模型文件」的要求。
> 获取方式：**B 站工房** [https://gf.bilibili.com/item/detail/1109618072](https://gf.bilibili.com/item/detail/1109618072)（作者主页 [https://space.bilibili.com/13737731](https://space.bilibili.com/13737731)）。

## 插件上游

- [A8Chann/dsh-pet-live2d](https://github.com/A8Chann/dsh-pet-live2d) — MIT License，
  Copyright (c) 2026 A8Chann
- 本仓库是它的个人修改版，改动明细见 [MODIFICATIONS.md](./MODIFICATIONS.md)

## Live2D 运行时

- `lib/live2d-vendor.js` — Live2D Cubism 运行时，沿用上游分发方式，
  使用需遵守 Live2D 的 SDK 许可条款。

## 示例宠物

- `pets/ds-whale-girl/` — 上游自带的示例宠物，随 MIT 包分发。
