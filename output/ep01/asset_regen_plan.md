# Asset Regen Plan · ep01《血尸》

## 重跑目标

```text
本轮重跑服务哪一集：ep01《血尸》
本轮优先保障哪些 Clip：04 老三被呵斥、06 拉绳反力、08 断手与血红东西、12 帛片与第二怪脸
本轮不追求什么：不追求每张图都是插画成片；优先让人物可识别、空间可调度、道具可操作。
```

## 人物资产

| 优先级 | 角色 | 资产类型 | 文件名 | 用途 | 阻塞哪些 Clip | 状态 |
|---|---|---|---|---|---|---|
| P0 | 老三 | identity | char_老三_identity.png | 锁定主角脸、体型、服装 | 04-12 | 待跑 |
| P0 | 老三 | expression | char_老三_expression.png | 不服、害怕、紧张、决绝等表演参考 | 04-12 | 待跑 |
| P0 | 老三 | state_variant | char_老三_tired.png | 中毒濒死状态 | 12 | 待跑 |
| P0 | 老二·独眼二伢子 | identity | char_老二_identity.png | 锁定独眼、体型、服装 | 03-04 | 待跑 |
| P0 | 老烟头 | identity | char_老烟头_identity.png | 锁定权威老人外观 | 02-04 | 待跑 |
| P0 | 大胡子 | identity | char_大胡子_identity.png | 锁定父亲 / 体力担当外观 | 02-04 | 待跑 |
| P1 | 血尸 | identity | char_血尸_identity.png | 锁定血尸整体外观 | 08-11 | 待跑 |
| P1 | 血尸 | state_variant | char_血尸_reveal.png | 林地暗部局部揭示状态 | 08-09 | 待跑 |
| P1 | 第二实体怪脸 | state_variant | char_第二实体怪脸_partial.png | 结尾局部无瞳怪脸 | 12 | 待跑 |

## 场景资产

| 优先级 | 场景 | 资产类型 | 文件名 | 用途 | 阻塞哪些 Clip | 状态 |
|---|---|---|---|---|---|---|
| P0 | 盗洞口 | establish | scene_盗洞口_establish.png | 建立洞口、土堆、周边地面关系 | 04-07 | 待跑 |
| P0 | 盗洞口 | action_area | scene_盗洞口_action_area.png | 四人分工、争执、老三被留外侧 | 04 | 待跑 |
| P0 | 盗洞口 | mechanism_area | scene_盗洞口_rope_mechanism.png | 拉绳、洞口、守位、绳线方向 | 05-07 | 待跑 |
| P0 | 荒野林地 | action_area | scene_荒野林地_action_area.png | 老三逃跑、停下、搏斗 | 08-11 | 待跑 |
| P1 | 荒野林地 | reveal_area | scene_荒野林地_reveal_area.png | 血尸从背后树间出现 | 08-09 | 待跑 |
| P1 | 荒野林地 | mechanism_area | scene_荒野林地_stump_area.png | 绊倒、贴地装死、被踩过 | 11 | 待跑 |
| P1 | 镖子岭土丘 | establish | scene_镖子岭土丘_establish.png | 开场土丘地理规模 | 01-03 | 待跑 |
| P1 | 镖子岭土丘 | action_area | scene_镖子岭土丘_shovel_area.png | 四人围铲定性、顶撞 | 01-03 | 待跑 |

## 道具资产

| 优先级 | 道具 | 资产类型 | 文件名 | 用途 | 阻塞哪些 Clip | 状态 |
|---|---|---|---|---|---|---|
| P0 | 土耗子 | identity | prop_土耗子_identity.png | 锁定不是普通绳子 | 04-08 | 待跑 |
| P0 | 土耗子 | use_state | prop_土耗子_tail_grip.png | 老三双手握尾端 | 04-06 | 待跑 |
| P0 | 土耗子 | mechanism_state | prop_土耗子_taut_rope.png | 拉绳受力、反向拖拽 | 06 | 待跑 |
| P0 | 土耗子 | mechanism_state | prop_土耗子_bundle.png | 从洞中弹出 / 怀抱 bundle | 07-08 | 待跑 |
| P0 | 匣子炮 | identity | prop_匣子炮_identity.png | 锁定旧毛瑟 C96 外观 | 03、09-10 | 待跑 |
| P1 | 匣子炮 | use_state | prop_匣子炮_handheld.png | 老三持枪后退 | 09-10 | 待跑 |
| P1 | 匣子炮 | mechanism_state | prop_匣子炮_jammed.png | 枪卡壳 | 10 | 待跑 |
| P1 | 洛阳铲铲头 | identity | prop_洛阳铲铲头_identity.png | 开场异常物 | 01-02 | 待跑 |
| P1 | 旱烟枪 | identity | prop_旱烟枪_identity.png | 老烟头标志动作 | 02-04 | 待跑 |
| P1 | 古帛片 | identity | prop_古帛片_identity.png | 结尾线索 | 12 | 待跑 |
| P1 | 老二断臂线索物 | story_variant | prop_老二断臂_fist.png | Clip 08 认出线索，小面积处理 | 08 | 待跑 |
| P1 | 老二断臂握帛片 | story_variant | prop_老二断臂_cloth.png | Clip 12 取帛片 | 12 | 待跑 |

## 通过标准

```text
人物：脸、体型、服装、关键识别点清楚；老二独眼必须稳定；老三要有表演可读性。
场景：空间可调度；洞口、绳线方向、守位、黑暗威胁方向清楚。
道具：外观清楚；土耗子必须区别于普通绳子；匣子炮必须是旧枪；关键状态可操作。
```

## 暂缓资产

```text
- 远景大氛围图可暂缓，优先 action_area 和 mechanism_area。
- 非关键配角表情图可暂缓，主角老三 expression 优先。
```
