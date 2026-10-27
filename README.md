# Design Clone Skill

从网站、截图、Figma 或前端代码中提取可复用设计规则，让后续 AI 生成的界面延续原产品的视觉和交互体系。

**版本：0.2**

## 能力

- 生成 `design.md`：颜色、字体、间距、组件、布局和素材规则。
- 目标明确时生成 `target.md` 与压力测试清单。
- 按需生成组件清单、多页面登记表、设计 QA 记录和 AI 使用提示词。
- 支持中文界面、局部修改、复杂工作台及可编辑 Figma 场景。

## 安装

下载并解压 `design-clone-skill-0.2.zip`，将其中的 `design-clone-skill` 文件夹放入 `~/.codex/skills/`。已存在同名技能时，请先备份后替换。重新打开 Codex 会话以加载技能。

## 使用

```text
使用 $design-clone-skill，分析我提供的网站链接、截图或设计文件，
生成 design.md；目标页面是团队资产管理工作台，
请同时生成 target.md、组件清单与压力测试清单。
```

输入应包含设计证据；如果需要目标页面规则，请说明页面类型、主要用户和任务。Figma 读写需要在运行环境中另行配置相应工具。本技能本身不包含登录信息或外部服务配置。

## 标准包结构

```text
design-clone-skill/
├── SKILL.md
├── agents/openai.yaml
├── references/
│   ├── core-rules.md
│   ├── design-md-template.md
│   ├── target-md-template.md
│   └── consumer-prompts.md
└── README.md
```

`SKILL.md` 为标准入口；`agents/openai.yaml` 为 Codex 界面元数据；`references/` 为按需加载的规则和模板。技能无需安装运行时依赖。

## 授权

本仓库暂未指定开源许可证。公开可见不等于授予再分发或商业使用许可。
