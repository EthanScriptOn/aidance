# Asset Manifest · ep01《血尸》

## Episode

```text
集数：ep01
剧本路径：script/血尸章节.txt
时代段：era_前传
本集一句话目标：用血土、下洞、逃亡和第二怪脸建立前传盗墓事件的恐怖钩子。
当前资产状态：旧图片准备删除并重跑；视频 prompt 暂不应视为可直接执行，直到 asset_regen_plan 完成。
```

## 复用资产

| 类型 | 名称 | 规范路径 | 本集用途 | 注意事项 |
|---|---|---|---|---|
| 角色 | 老烟头 | assets/images/char_老烟头_main.png | 权威判断、分工、下洞前压场 | 出镜时常与旱烟枪同用 |
| 角色 | 大胡子 | assets/images/char_大胡子_main.png | 老二父亲、群像压力、老三求救失败对象 | 不要与老二混淆 |
| 角色 | 老二·独眼二伢子 | assets/images/char_老二·独眼二伢子_main.png | 顶撞、呵斥老三、洞下事件前归属 | 独眼是关键识别点 |
| 角色 | 老三 | assets/images/char_老三_main.png | 本集后半主视角 | 从被留下到逃亡、搏斗 |
| 角色 | 老三 tired | assets/images/char_老三_tired.png | 结尾中毒濒死段落 | Clip 12 使用 |
| 角色 | 血尸 | assets/images/char_血尸_main.png | 林地追击与搏斗威胁 | 不要过早全亮 |
| 角色 | 第二实体怪脸 | assets/images/char_第二实体怪脸_partial.png | 结尾终极揭示 | 只显示局部怪脸 |
| 场景 | 镖子岭荒野土丘 | assets/images/scene_镖子岭土丘_main.png | 开场、土丘群像 | 夜晚冷月光 |
| 场景 | 盗洞口 | assets/images/scene_盗洞口_main.png | 下洞、守绳、拉绳 | 洞内纯黑 |
| 场景 | 荒野林地 | assets/images/scene_荒野林地_main.png | 逃跑、血尸、结尾 | 林地深处大面积黑 |
| 道具 | 洛阳铲铲头 | assets/images/prop_洛阳铲铲头_main.png | 血土钩子 | 异常湿痕是唯一暖色 |
| 道具 | 旱烟枪 | assets/images/prop_旱烟枪_main.png | 老烟头压场与阻挡动作 | 与老烟头同用 |
| 道具 | 匣子炮 | assets/images/prop_匣子炮_main.png | 老二逞能、老三搏斗 | 旧枪，不是现代枪 |
| 道具 | 土耗子 | assets/images/prop_土耗子_main.png | 守绳、拉绳、bundle | Clip 04-08 连续关键物 |
| 道具 | 老二断臂·握拳 | assets/images/prop_老二断臂_fist.png | Clip 08 认出线索 | 小面积、非写实、非血腥铺陈 |
| 道具 | 老二断臂·握帛片 | assets/images/prop_老二断臂_cloth.png | Clip 12 取帛片 | 小面积线索物 |
| 道具 | 古帛片 | assets/images/prop_古帛片_main.png | 结尾 MacGuffin | 不要放大成主角 |

## 新增资产需求

| 类型 | 暂定名称 | 出现原文范围 | 为什么需要 | 生成前是否阻塞视频 |
|---|---|---|---|---|
| 无 | — | — | ep01 当前可用既有资产覆盖 | 否 |

## 变体需求

| 资产 | 变体名 | 触发剧情 | 生效范围 | 是否需要新图 |
|---|---|---|---|---|
| 老三 | tired | 被血尸踩背后中毒 | Clip 12 | 已有 |
| 老二 | 断臂状态 / 断臂道具 | 洞下遭遇后土耗子带出线索 | Clip 08、Clip 12 | 已有 |

## 关键道具归属变化

| 道具 | 起始归属 | 变化动作 | 结束归属 | 生效 Clip |
|---|---|---|---|---|
| 土耗子 | 老二带前端、老三守尾端 | 洞下喊拉，老三拉绳，bundle 弹出 | 老三怀抱 bundle 逃跑 | Clip 07 |
| 匣子炮 | 老二 / 家族旧枪 | 后续逃亡中老三使用 | 老三临时持有 | Clip 09-10 |
| 古帛片 | 断臂线索物手中 | 老三艰难取出塞入袖中 | 老三袖中 | Clip 12 |

## 暂不进入视频生成的问题

```text
- 断臂类线索在视频 prompt 中尽量写成“小面积深褐色线索物”，以人物 reaction 为主。
- 洞内人物不直接显示，洞内信息用声音、绳索受力、枪火一闪表达。
```

## 本集资产结论

```text
可以直接生成的 Clip：资产图重跑完成后，01-12 都可生成
需要先补资产的 Clip：当前所有涉及可见人物、场景、关键道具的 Clip 都等待重跑资产
```

## 资产重跑入口

```text
重跑计划：output/ep01/asset_regen_plan.md
```
