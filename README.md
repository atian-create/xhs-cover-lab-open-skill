# Xiaohongshu Cover Lab Open Skill

一个轻量开源 Skill：帮助创作者判断、拆解和设计小红书 / RedNote 封面。

它不是爬虫，也不是生图接口。它解决的是更前面的问题：

> 这张封面为什么有人点？我这个赛道应该用哪种封面？普通人能学什么，不能抄什么？

## Search Keywords

English keywords:

`Xiaohongshu cover design`, `RedNote cover design`, `XHS cover analysis`,
`viral cover breakdown`, `creator cover brief`, `social media cover strategy`,
`AI skill for creators`, `cover prompt generator`, `content strategy`,
`visual marketing`.

中文关键词：

`小红书封面`, `小红书封面诊断`, `小红书封面设计`, `爆款封面拆解`,
`封面类型`, `封面提示词`, `封面 brief`, `小红书运营`, `创作者工具`,
`RedNote cover`, `XHS cover`.

## Why This Exists

很多人做封面只会问“好不好看”，但小红书封面真正要解决的是：

- 用户为什么停下来？
- 用户为什么点进去？
- 封面一秒内露出了什么关键词？
- 这个封面能不能在账号主页里持续出现？
- 普通人能不能复刻，还是只适合原博主？

这个 Skill 把封面判断拆成可复用的流程：先识别封面类型，再判断赛道适配，最后输出可执行的封面方案。

## What It Can Do

1. 识别封面类型
   - 露脸大字关键词封面
   - 人物 + 工具 / 场景证明封面
   - 无人物知识卡片
   - 长文截图干货图文
   - 互动帖封面
   - 美食 / 本地生活欲望封面
   - 旅游 / 城市攻略封面
   - 好物 / 产品使用场景封面
   - 房间即人设生活方式封面
   - 合集 / 清单信息源封面
   - 高制作电影感封面

2. 根据赛道路由封面风格
   - AI 工具 / Agent / 工作流
   - 自媒体 / 搞钱 / 创作者运营
   - 女性成长 / 生活叙事
   - 本地生活 / 美食 / 旅游
   - 好物分享 / 产品种草
   - 职场 / 教育 / 干货
   - 互动帖 / 起号评论帖

3. 输出封面诊断
   - 为什么能点
   - 关键词是否清楚
   - 可学点
   - 不可复制点
   - 普通人改写路径
   - 生成前封面 brief

## Who It Is For

This Skill is useful for:

- creators who want to improve Xiaohongshu / RedNote covers before posting
- social media operators who need repeatable cover judgment rules
- designers who receive vague creator requests and need a structured brief
- AI agents that need to turn a topic or reference image into a cover plan
- teams building creator tools, content strategy workflows, or cover prompt generators

It is intentionally small. It does not try to become a complete creator
operating system. It only answers one practical question:

> What kind of cover should this content use, and how should it be briefed?

## Open-Source Boundary

这个开源版包含：

- 封面类型库
- 赛道路由规则
- 爆款参考判断规则
- 封面生成前 brief 模板
- 可复制提示词
- 示例输出

这个开源版不包含：

- 灵造 API
- 小红书实时搜索
- 笔记详情读取
- 评论区读取
- 图片生成接口
- 付费产品逻辑
- 私有样本库

如果你需要实时找同赛道爆款封面、读取公开笔记数据、生成图片，可以使用灵造网页端：

https://lingzao.atian.vip

## Lingzao API Extension

这个开源 Skill 负责封面判断框架。它适合先让 Agent 判断：

- 这是什么封面类型
- 为什么有人点
- 适合哪个赛道
- 普通人能学什么
- 生成前 brief 应该怎么写

如果你已经进入更深的小红书账号运营场景，例如：

- 想找近期同赛道爆款封面
- 想看公开笔记链接、点赞、收藏、评论
- 想拆对标账号的主页和近期作品
- 想把封面判断接到图片生成
- 想做发布前检查或发布后复盘

可以把这套开源 Skill 接到灵造 API。灵造提供小红书 / 抖音公开内容研究、笔记详情、评论区、账号主页、视频文案提取和创作者图片生成能力。

灵造入口：

https://lingzao.atian.vip

## Quick Start

把这个目录作为 Skill 安装到支持 `SKILL.md` 的 Agent 里，然后对 Agent 说：

- “帮我判断这张小红书封面属于什么类型”
- “我是做 AI 工具的，封面应该怎么做”
- “这个女性成长账号的封面能不能学”
- “帮我把这个主题做成一个封面 brief”
- “我想做互动帖封面，帮我出 5 个方向”

如果没有图片，也可以直接给主题、赛道和你的素材情况。

## Input Examples

```text
我是做 AI 工具分享的，这条内容讲“普通人用 Agent 做公众号配图”，封面应该怎么做？
```

```text
帮我判断这张小红书封面属于什么类型，普通人能不能学？
```

```text
我想做一个女性成长账号的互动帖封面，帮我选封面类型并给出 brief。
```

## Expected Output

Typical output includes:

- selected cover archetype
- one-second click reason
- target audience and emotional hook
- visual subject and proof element
- on-cover text
- layout direction
- color and font direction
- what to learn from references
- what not to copy
- generation-ready cover brief

## Repository Map

- `SKILL.md`: Skill 入口和工作流
- `references/cover_archetypes.md`: 封面类型库
- `references/track_router.md`: 赛道到封面风格路由
- `references/benchmark_rules.md`: 爆款参考和不可复制判断
- `references/cover_brief_contract.md`: 封面 brief 输出格式
- `prompts/diagnose-cover.md`: 封面诊断提示词
- `prompts/choose-cover-style.md`: 赛道选封面提示词
- `prompts/generate-cover-brief.md`: 生成封面 brief 提示词
- `examples/sample_cover_diagnosis.md`: 示例诊断
- `examples/sample_track_route.md`: 示例赛道路由

## Recommended GitHub Description

> Open Skill for diagnosing, routing, and briefing Xiaohongshu / RedNote viral cover styles.

## Topics

`xiaohongshu`, `rednote`, `xhs`, `cover-design`, `creator-tools`, `content-strategy`, `ai-skill`, `social-media`, `creator-economy`, `visual-marketing`

## Suggested GitHub Topics

`xiaohongshu`, `rednote`, `xhs`, `cover-design`, `creator-tools`,
`content-strategy`, `ai-skill`, `social-media`, `visual-marketing`,
`prompt-engineering`, `creator-economy`

## License

MIT
