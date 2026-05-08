# Asset Manifest · ep01

## Episode

```text
集数：ep01
剧本路径：script/血尸章节.txt
时代段：era_前传（约1960-1970年代，湖南农村，长沙镖子岭）
本集一句话目标：四个土夫子从“下洞取宝”的贪念进入“地底怪物真实存在”的生死追逐，老三被迫接住断臂线索并在中毒濒死时看见第二实体。
```

## 复用资产

| 类型 | 名称 | 规范路径 | 本集用途 | 注意事项 |
|---|---|---|---|---|
| 角色 | 老烟头 | assets/images/characters/char_老烟头_identity.png | Clip 01-03 土丘判断、训斥、分工 | 老烟头出镜且旱烟枪可见时叠用 `assets/images/props/prop_旱烟枪_identity.png`。当前为 新流程待跑图，不是新流程 identity/expression 拆分图。 |
| 角色 | 大胡子 | assets/images/characters/char_大胡子_identity.png | Clip 02-03 父权压制老二、无视老三求救 | 当前只有 identity 近似图，缺 expression。 |
| 角色 | 老二·独眼二伢子 | assets/images/characters/char_老二_identity.png | Clip 02-03 顶嘴、揪老三耳朵；Clip 08-10 以断臂/枪/绳的结果链存在 | 断臂后需同时上传主图与断臂变体。当前主图可测，缺 expression。 |
| 角色 | 老二·断臂状态 | assets/images/char_老二_断臂.png | Clip 08-10 结果确认；Clip 14 断臂握帛关联 | registry 标为已锁，但 characters.md 仍写待生成，两处状态冲突；正式流程需复核或重跑。 |
| 角色 | 老三 | assets/images/characters/char_老三_identity.png | Clip 03-13 主视角行动 | 主角表情变化最多，缺 expression 会影响人物冲突戏。 |
| 角色 | 老三·疲惫/中毒末态 | assets/images/characters/char_老三_tired.png | Clip 13-15 被踩后中毒、爬行取帛片、抬头见怪脸 | 已有变体，可临时测；正式需要 state_variant 命名与主图图生图一致性确认。 |
| 角色 | 血尸 | assets/images/characters/char_血尸_identity.png | Clip 10-13 林地蹲伏、扑击、受枪击、踩过老三 | 有 identity，但缺 reveal/动作姿态参考；动作片段需补 state_variant 或动作参考。 |
| 角色 | 第二实体 / 无瞳怪脸 | assets/images/characters/char_第二实体怪脸_partial.png | Clip 15 最终俯压揭示 | 仅允许局部揭示，不做完整身体。 |
| 场景 | 镖子岭荒野土丘 | assets/images/scenes/scene_镖子岭土丘_shovel_area.png | Clip 01-04 土丘顶面、洛阳铲、盗洞前分工 | 旧九宫格已归档，新流程需重跑 establish/action_area。 |
| 场景 | 盗洞口 | assets/images/scenes/scene_盗洞口_action_area.png | Clip 04-08 守绳、听声、拔河、弹出 | 旧六格图已归档，新流程需重跑 action_area/mechanism_area/reveal_area。 |
| 场景 | 荒野林地 | assets/images/scenes/scene_荒野林地_action_area.png | Clip 09-15 逃跑、断臂确认、血尸对峙、树墩绊倒、取帛片 | 旧九宫格已归档，新流程需重跑 establish/action_area/reveal_area/mechanism_area。 |
| 道具 | 洛阳铲铲头 | assets/images/props/prop_洛阳铲铲头_identity.png | Clip 01 深红褐渗出液视觉钩子 | 缺 story_variant：铲口带深红褐湿痕的近景使用态可从当前图临时测。 |
| 道具 | 旱烟枪 | assets/images/props/prop_旱烟枪_identity.png | Clip 01-03 老烟头敲烟枪、挡大胡子手 | registry 标已锁，props.md 写待生成，状态冲突；正式需复核或重跑 identity/use_state。 |
| 道具 | 土耗子 | assets/images/props/prop_土耗子_identity.png | Clip 04-09 分工、拉绳、绑腰、弹出、怀抱 | 当前为新流程待跑图，正式 Clip 04-09 均阻塞。 |
| 道具 | 匣子炮 | assets/images/props/prop_匣子炮_identity.png | Clip 08、11-12 老二传枪、老三持枪、卡壳、抛砸 | registry 标已锁，props.md 写待生成，状态冲突；需补 handheld/jammed 机制图。 |
| 道具 | 老二断臂·握拳 | assets/images/props/prop_老二断臂_fist.png | Clip 09 断手确认 | registry 标已锁，props.md 写待生成，状态冲突；正式需复核或重跑 story_variant。 |
| 道具 | 老二断臂·握帛片 | assets/images/props/prop_老二断臂_cloth.png | Clip 14 掰手取帛 | registry 标已锁，props.md 写待生成，状态冲突；正式需复核或重跑 story_variant。 |
| 道具 | 古帛片 | assets/images/props/prop_古帛片_identity.png | Clip 14 线索入袖 | 已有 identity，需 use_state：从断臂掌心抽出、塞入袖中。 |

## 新增资产需求

| 类型 | 暂定名称 | 资产类型 | 出现原文范围 | 为什么需要 | 生成前是否阻塞视频 |
|---|---|---|---|---|---|
| 角色 | 老三_expression | expression | 老三抗议、求救、惊恐、咬牙、濒死 | 本集主视角靠连续表情成立，只有 main/tired 不够稳定 | 是，阻塞 Clip 03、05、06、09-15 的正式版 |
| 角色 | 老二_expression | expression | 顶嘴、偷笑、发火、揪耳朵 | Clip 02-03 是人物冲突戏，独眼、偷笑、暴怒不能漂 | 是，阻塞 Clip 02-03 正式版 |
| 角色 | 大胡子_expression | expression | 瞪老二、抬手打、去收拾家伙 | 需要父亲压制和拒绝救场的表演可读 | 否，可用 main 临时测 |
| 角色 | 老烟头_expression | expression | 不怒反笑、训斥、挡手、发号施令 | 需要“老练压场”而不是普通老人 | 否，可用 main 临时测 |
| 角色 | 血尸_state_attack | state_variant | 林地蹲伏、站起、扑击、踩过 | 现有 identity 不保证蹲伏/扑击/脚踩动作一致 | 是，阻塞 Clip 10-13 正式版 |
| 场景 | 镖子岭土丘_establish | establish | 开篇四人蹲在土丘上 | 新流程要求建立地理与顶面尺度，不应只依赖九宫格 main | 否，需等待新资产或仅做极粗临时测试 |
| 场景 | 镖子岭土丘_action_area | action_area | 四人围铲、争执、分工 | 人物调度需要明确站位和洞口/铲子关系 | 是，阻塞 Clip 01-04 正式版 |
| 场景 | 盗洞口_action_area | action_area | 老三守洞口喊话 | 需要老三在洞口旁的表演区域 | 是，阻塞 Clip 05-06 正式版 |
| 场景 | 盗洞口_mechanism_area | mechanism_area | 拉绳、绑腰、反力、弹出 | Clip 07-08 靠绳力学成立，必须有洞口-绳-木楔机制位 | 是，阻塞 Clip 07-08 正式版 |
| 场景 | 盗洞口_reveal_area | reveal_area | 洞内咯咯声和画外未知 | 需要纯黑洞口作为威胁来源 | 否，需等待新资产或仅做极粗临时测试 |
| 场景 | 荒野林地_establish | establish | 老三跑出二里地停下 | 需要建立土丘到林地的逃离空间 | 否，需等待新资产或仅做极粗临时测试 |
| 场景 | 荒野林地_action_area | action_area | 停下看断手、持枪对峙 | 林地人物轴线必须稳定，避免血尸和老三换位 | 是，阻塞 Clip 09-12 正式版 |
| 场景 | 荒野林地_mechanism_area | mechanism_area | 树墩绊倒、趴地被踩、爬向断臂 | 需要贴地、树墩、来时路、身体低位机制 | 是，阻塞 Clip 13-14 正式版 |
| 场景 | 荒野林地_reveal_area | reveal_area | 血尸蹲伏、第二实体俯压 | 威胁揭示区必须与老三低位方向一致 | 是，阻塞 Clip 10、15 正式版 |
| 道具 | 土耗子_use_state | use_state | 老三拉住尾巴、抱住弹回物 | 当前占位图只能锁外观，不锁握持/怀抱状态 | 是，阻塞 Clip 04、07-09 正式版 |
| 道具 | 土耗子_mechanism_state | mechanism_state | 绳子被反拉、绑腰僵持、嗖地弹出 | 物理因果是 Clip 07-08 核心，必须锁受力状态 | 是，阻塞 Clip 07-08 正式版 |
| 道具 | 匣子炮_use_state | use_state | 老三拔枪、连发、抡枪砸出 | 需要持枪姿势稳定 | 是，阻塞 Clip 11-12 正式版 |
| 道具 | 匣子炮_mechanism_state | mechanism_state | 喀嚓卡壳 | Clip 12 转折靠卡壳成立 | 是，阻塞 Clip 12 正式版 |
| 道具 | 老二断臂_fist_story_variant | story_variant | 土耗子上勾着断手 | 现有状态冲突，且需勾挂关系 | 是，阻塞 Clip 09 正式版 |
| 道具 | 老二断臂_cloth_story_variant | story_variant | 断手握着古帛片 | 取帛片的关键揭示，需要手指半握与帛片露出 | 是，阻塞 Clip 14 正式版 |
| 道具 | 古帛片_use_state | use_state | 掰出、塞进袖子 | MacGuffin 归属变化必须可读 | 是，阻塞 Clip 14 正式版 |

## 变体需求

| 资产 | 变体名 | 触发剧情 | 生效范围 | 是否需要新图 |
|---|---|---|---|---|
| 老三 | expression：抗议/求救/惊恐/咬牙/濒死 | 被排除、洞口听声、看断臂、血尸贴脸、尸毒发作 | Clip 03、05-15 | 是 |
| 老三 | 持枪状态 | 接到老二从洞内传出的匣子炮后 | Clip 11-12 | 是，角色+道具叠用可先测，正式补 state_variant 或 use_state |
| 老三 | 中毒末态 | 血尸踩背后 | Clip 13-15 | 已有 `assets/images/characters/char_老三_tired.png`，需复核一致性 |
| 老二 | 断臂状态 | 洞内遭遇后 | Clip 09、14 | 已有但 registry/props 状态冲突，需复核或重跑 |
| 血尸 | 蹲伏/扑击/踩过 | 林地追击 | Clip 10-13 | 是 |
| 土耗子 | 拉绳/绑腰/弹出/怀抱 | 老三守绳到逃跑 | Clip 04、07-09 | 是 |
| 匣子炮 | 手持/卡壳/抛砸 | 老三反击失败 | Clip 11-12 | 是 |
| 古帛片 | 从断臂掌心取出/入袖 | 老三濒死保存线索 | Clip 14 | 是 |

## 关键道具归属变化

| 道具 | 起始归属 | 变化动作 | 结束归属 | 生效 Clip |
|---|---|---|---|---|
| 洛阳铲铲头 | 四人共用工具 / 地面 | 被四人盯住，渗出深红褐液体成为危险信号 | 仍在土丘顶面，成为“下方有血尸”的视觉证据 | Clip 01 |
| 旱烟枪 | 老烟头 | 敲地、挡住大胡子的手、压住冲突 | 老烟头继续持有，成为权威动作锚点 | Clip 01-03 |
| 土耗子 | 团队工具 / 老二殿后任务 | 老烟头分配给老三拉尾巴；老三拉、绑腰、接住弹出物 | 老三怀抱，带离盗洞口 | Clip 04-09 |
| 匣子炮 | 老二 | 洞内枪响后随土耗子结果链传至地面；老三在林地拔出连发 | 老三短暂持有，卡壳后抡出丢失 | Clip 08、11-12 |
| 老二断臂·握拳 | 老二身体的一部分 | 被土耗子从洞内带出，挂在绳/勾上 | 老三发现并认出 | Clip 09 |
| 老二断臂·握帛片 | 老二断臂 | 老三爬过去掰开手指 | 帛片从断臂转移给老三 | Clip 14 |
| 古帛片 | 老二断臂手心 | 老三掰出并塞入袖中 | 老三 | Clip 14 |

## 暂不进入视频生成的问题

```text
- 正式版不应使用旧九宫格/六宫格资产；需要按 establish/action_area/mechanism_area/reveal_area 重跑。
- `registry.md` 与 `characters.md` / `props.md` 对若干资产状态不一致：旱烟枪、匣子炮、老二断臂、老二断臂道具在 registry 中为已锁或已有文件，但细表仍写待生成。冷启动验收应视为“需要复核或重跑”，不能默认为无阻塞。
- `assets/images/props/prop_土耗子_identity.png` 明确是新流程待跑图，Clip 04、07、08、09 可做临时测试，但正式视频被阻塞。
- 血尸当前只有 identity，不足以稳定生成蹲伏、扑击、踩背；Clip 10-13 正式视频被阻塞。
- 第二实体只能局部揭示，不得扩写成完整怪物角色或全身对峙。
```

## 本集资产结论

```text
可以直接临时测试的 Clip：
- Clip 01 铲头渗液
- Clip 02 土丘争执
- Clip 03 老三被压服
- Clip 05 洞口喊话
- Clip 06 洞内咯咯声
- Clip 15 第二实体局部压脸（只测局部威胁，不测完整动作）

需要先补资产或复核后才能正式生成的 Clip：
- Clip 04 分工落位：土耗子 use_state、土丘/盗洞口 action_area
- Clip 07 拔河反力：盗洞口 mechanism_area、土耗子 mechanism_state
- Clip 08 枪响弹出：土耗子 mechanism_state、匣子炮 use_state、老二断臂状态复核
- Clip 09 断臂确认：荒野林地 action_area、土耗子 use_state、老二断臂_fist story_variant
- Clip 10 血尸回头初现：荒野林地 reveal_area、血尸蹲伏状态
- Clip 11 贴脸开枪：血尸攻击状态、匣子炮 use_state
- Clip 12 卡壳翻盘：匣子炮 mechanism_state、血尸持续威逼状态
- Clip 13 树墩绊倒被踩：荒野林地 mechanism_area、血尸踩踏状态
- Clip 14 取帛片：老三中毒末态复核、老二断臂_cloth story_variant、古帛片 use_state

图片需要重跑/补跑：
- 人物：老三 expression；老二 expression；老烟头 expression；大胡子 expression；血尸 attack/step state_variant；老二断臂状态复核或重跑。
- 场景：镖子岭土丘 establish/action_area；盗洞口 action_area/mechanism_area/reveal_area；荒野林地 establish/action_area/mechanism_area/reveal_area。
- 道具：土耗子 identity 占位图替换、use_state、mechanism_state；匣子炮 identity 状态复核、use_state、mechanism_state；老二断臂 fist/cloth story_variant 复核或重跑；古帛片 use_state；旱烟枪 identity/use_state 状态复核。
```

## 资产重跑入口

```text
output/ep01/asset_regen_plan.md
```
