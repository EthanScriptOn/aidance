# Asset Generation Principles

资产图的目的不是“好看的设定图”，而是让后续视频模型稳定完成三件事：

```text
人物：识别是谁
场景：知道在哪里拍、人物站哪里、危险从哪里来
道具：看懂关键物如何被使用
```

## 第一性原理

每张资产图必须回答一个生成问题：

```text
这张图在视频生成时负责锁什么？
```

如果回答不出来，就不要生成这张图。

## 人物资产

人物资产解决“是谁”和“现在处于什么表演状态”。

### 必要类型

| 类型 | 目的 | 推荐画面 |
|---|---|---|
| identity | 锁定脸、体型、服装、关键识别点 | 纯白 / 浅灰背景，正面 + 侧面 + 背面，全身稳定站姿 |
| expression | 锁定常用表情和半身可读性 | 半身 / 胸像，3-5 个表情小格 |
| state_variant | 锁定剧情状态变化 | 受伤、疲惫、换装、中毒、持物等 |

### 命名

```text
char_角色名_identity.png
char_角色名_expression.png
char_角色名_状态名.png
```

示例：

```text
char_老三_identity.png
char_老三_expression.png
char_老三_tired.png
```

## 场景资产

场景资产解决“在哪里拍”和“空间如何调度”。

不要只生成一张氛围大图。重要场景至少拆成拍摄位参考。

### 必要类型

| 类型 | 目的 | 推荐画面 |
|---|---|---|
| establish | 建立地理关系、规模、方向 | 大空间，地形和关键区域清楚 |
| action_area | 人物主要表演和对话区域 | 中景 / 中远景，能站人、能调度 |
| mechanism_area | 关键动作机制区域 | 洞口、绳索、台阶、障碍、门口等可操作空间 |
| reveal_area | 威胁或秘密出现区域 | 黑暗方向、背后空间、树间、门缝等 |

### 命名

```text
scene_场景名_establish.png
scene_场景名_action_area.png
scene_场景名_mechanism_area.png
scene_场景名_reveal_area.png
```

示例：

```text
scene_盗洞口_establish.png
scene_盗洞口_action_area.png
scene_盗洞口_rope_mechanism.png
scene_盗洞口_black_mouth.png
```

## 道具资产

道具资产解决“是什么”和“怎么用”。

### 必要类型

| 类型 | 目的 | 推荐画面 |
|---|---|---|
| identity | 锁定外观 | 白底或简背景，完整物体，尺度清楚 |
| use_state | 锁定被拿、被握、被装入、被打开等状态 | 带手部或局部动作参考 |
| mechanism_state | 锁定关键力学或功能 | 绳子受力、枪卡壳、bundle 弹出、钩住线索 |
| story_variant | 锁定剧情变化后的道具状态 | 断裂、藏入袖中、挂着线索等 |

### 命名

```text
prop_道具名_identity.png
prop_道具名_使用状态.png
prop_道具名_机制状态.png
```

示例：

```text
prop_土耗子_identity.png
prop_土耗子_tail_grip.png
prop_土耗子_bundle.png
prop_土耗子_hook_clue.png

prop_匣子炮_identity.png
prop_匣子炮_handheld.png
prop_匣子炮_jammed.png
```

## 生成优先级

### 第一层：身份与基础空间

```text
主要人物 identity
主要场景 establish / action_area
关键道具 identity
```

### 第二层：高频表演和动作机制

```text
主角 expression
关键场景 mechanism_area
关键道具 use_state / mechanism_state
```

### 第三层：剧情状态变体

```text
角色受伤 / 疲惫 / 换装
怪物局部 reveal
关键线索物状态
```

## 进入视频生成的门槛

一个 Clip 可以进入 prompt 生成，必须满足：

```text
可见人物都有 identity 图
主要场景至少有匹配的拍摄位图
关键道具至少有 identity 图
如果 Clip 靠道具动作成立，必须有 use_state 或 mechanism_state 图
如果 Clip 靠表情成立，主角最好有 expression 图
```

不满足时，不要硬写视频 prompt，应先进入资产重跑计划。
