# Asset Registry

这是新流程的主资产注册表。旧流程资产文案已归档到：

```text
assets_legacy/
```

本注册表只回答多集连续性需要的最小问题：

```text
这个资产是什么？
它属于哪种生成用途？
图片是否已经锁定？
它阻塞哪些 Clip？
```

## 状态

| 状态 | 含义 |
|---|---|
| 待跑 | 还没有生成或尚未确认 |
| 候选 | 已生成但未最终确认 |
| 已锁定 | 可进入视频 prompt |
| 已弃用 | 不再进入主流程 |

## 人物资产

详见 [characters.md](characters.md)。

人物资产类型：

```text
identity：锁定脸、体型、服装、关键识别点
expression：锁定常用表演状态
state_variant：锁定剧情状态变化
```

## 场景资产

详见 [scenes.md](scenes.md)。

场景资产类型：

```text
establish：建立空间规模与地理关系
action_area：人物主要表演和调度区域
mechanism_area：关键动作机制区域
reveal_area：威胁或秘密出现区域
```

## 道具资产

详见 [props.md](props.md)。

道具资产类型：

```text
identity：锁定外观
use_state：锁定被拿、被握、被打开等使用方式
mechanism_state：锁定受力、卡壳、弹出等机制状态
story_variant：锁定剧情变化后的状态
```

## 目录规范

```text
assets/images/characters/
assets/images/scenes/
assets/images/props/
```

不要再使用 `main`、`main_new`、`final2` 这类模糊命名。

