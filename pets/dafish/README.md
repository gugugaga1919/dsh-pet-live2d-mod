# 大肥鱼（DeepSeek-chan）模型 —— 获取方式

本仓库**不再托管模型文件**，以遵守原作者「禁止擅自重新分发模型文件」的使用须知。

## 怎么获取

免费公开配布，原作者（原画及拆分）：**神宫凉子**

- **B 站主页**：[神宫凉子的个人空间](https://space.bilibili.com/13737731)（短链 https://b23.tv/8POy29x）—— 配布信息与获取方式以作者主页为准
- Live2D 建模：**霓虹猫_NeonNeko**
- 使用前请阅读随模型发布的《DeepSeek 免费 Live2D 模型使用须知》（本目录
  [LICENSE-usage-terms.txt](./LICENSE-usage-terms.txt) 为原文副本）

## 拿到模型后怎么在本仓库的插件里用

模型原始格式是 VTube Studio 用的（`.moc3/.model3.json/.cdi3.json/.physics3.json` + 贴图）。
转换成本仓库插件能读的宠物包，主要做三件事：

1. 所有文件路径改成 ASCII（原中文文件名会导致路由 404）；
2. 贴图压到最长边 2048（原 4096/8192 太大，显存与加载都吃不消）；
3. 生成 `pet.json` + `catalog.json`（`petManifestVersion: 2`、`renderer: "live2d"`），
   放到 `~/.dsh/pets/<id>/`。

本仓库的 [MODIFICATIONS.md](../../MODIFICATIONS.md) 与 `lib/client.js` 的注释里有完整说明。
