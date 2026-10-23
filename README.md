# 日式动漫一拍三 赛璐璐

用于人物图片生成、重绘与提示词编写的独立 Agent Skill。通过四张参考截图，提取清线稿、成组发片、简洁五官和赛璐璐分色的绘画方式，保留本次角色的身份、发型、服装与动作。

- **中文名称**：日式动漫一拍三 赛璐璐
- **技能标识**：`anime-on-threes-cel`
- **风格范围**：人物画法；背景、场景、镜头和照明由本次需求决定。

## 安装

在 Windows PowerShell 中克隆到 Codex 的技能目录：

```powershell
git clone https://github.com/Ruriy06/anime-on-threes-cel.git "$env:USERPROFILE\.codex\skills\anime-on-threes-cel"
```

使用自定义技能目录时，将目标路径替换为你的技能目录。其他支持 `SKILL.md` 的 Agent 可复制整个仓库目录，保留 `agents/` 和 `references/` 的相对路径。

## 使用

```text
使用 $anime-on-threes-cel，把这个角色重绘为“日式动漫一拍三 赛璐璐”画风。
保留角色的发型、服装、配饰与身份，背景使用纯白。
```

```text
按“日式动漫一拍三 赛璐璐”画风编写双人对话场景的生图提示词，
角色与场景采用我提供的设定，只迁移参考图中的人物画法。
```

需要实际生图时，由当前环境中可用且由用户选定的生图工具执行。引用画风截图时，应把相应图片作为实际图像输入传入工具。

## 文件

- [SKILL.md](SKILL.md)：技能入口与执行流程。
- [agents/openai.yaml](agents/openai.yaml)：中文展示名称和默认调用提示。
- [references/character-style.md](references/character-style.md)：人物画法、提示词与修正方法。
- [references/image-index.md](references/image-index.md)：四张参考截图的选择与使用范围。
- [references/images/manifest.json](references/images/manifest.json)：原图尺寸、来源文件名与 SHA-256。

## 参考图与验证状态

四张参考截图作为人物画法依据保留，图像像素未经修改；截图中的角色、场景、字幕与角标由原权利人享有相应权利。参考截图不代表本技能的生成结果。

当前提示词尚未经过实际生图验证。结构校验与参考图完整性检查不等同于画风复现验证。
