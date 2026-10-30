# A Way Out Simplified Chinese Patch

《逃出生天》（A Way Out）Steam Windows 版非官方简体中文补丁。

本补丁包含剧情字幕、界面、系统提示，以及中文所需的运行时字体子集。它只面向已拥有正版游戏的玩家，免费且与 Hazelight Studios、EA 和 Steam 无关。

## 适用版本

- Steam Windows 版《逃出生天》
- 游戏目录示例：`D:\Steam\steamapps\common\AWayOut`

## 安装

1. 退出游戏和 EA app。
2. 下载 [`release/AWayOut_SimplifiedChinese_v4_P.pak`](release/AWayOut_SimplifiedChinese_v4_P.pak)。
3. 将文件复制到 `AWayOut\Haze1\Content\Paks\`。
4. 将复制后的文件重命名为 `pakchunk0-WindowsNoEditor_P.pak`。
5. 从 Steam 启动游戏。

完整目标路径示例：

```text
D:\Steam\steamapps\common\AWayOut\Haze1\Content\Paks\pakchunk0-WindowsNoEditor_P.pak
```

## 卸载

删除 `AWayOut\Haze1\Content\Paks\pakchunk0-WindowsNoEditor_P.pak` 即可恢复英文。原版游戏默认没有这个 `_P.pak` 文件。

## 校验

当前补丁版本为 `v4`：

```text
SHA-256: 2B27947B518D3D41757845C3D33E5F6886E3234B459466D7613DD54FD34FB29A
```

也可查看 [SHA256SUMS.txt](SHA256SUMS.txt)。

## 制作方式

1. 导出游戏的 UE4 `Game.locres` 为可审校的 CSV。
2. 翻译并人工统一人名、界面术语和键鼠标签。
3. 将译文导回 locres，保留全部原始键与 Unreal 控制标签。
4. 为游戏实际使用的 GUI 字体生成仅含补丁所需字符的中文字形子集。
5. 按原版格式 `UE4 Pak V4 + Zlib` 打包为覆盖包。

已修正的已知问题包括：

- `RMB`、`LMB`、`Esc` 等键鼠标签被误译；现在均保留原始缩写。
- `Vincent` 被错误翻译为“文殊/文殊师利/温森特”，以及部分重复显示；现统一为“文森特”。

## 已知限制

这是基于初稿持续人工审校的社区补丁，完整剧情仍可能存在不够自然、语境不准确或遗漏的句子。请在 [Issues](../../issues) 提交截图、章节位置、英文原文与建议译文，便于后续修订。

## 版权说明

请勿将本仓库视为对游戏资源、文本或字体的权利声明或授权。补丁可能包含为兼容游戏而生成的派生数据；若权利人提出要求，维护者应配合修改或下架。请仅在拥有正版游戏的前提下使用。

