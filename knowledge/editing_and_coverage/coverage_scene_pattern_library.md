# 剪辑与镜头覆盖库

> 用途：回答“这场戏该如何组织镜头”。
> 说明：本库和 `generation_decision_library.md` 不同。`generation_decision_library.md` 解决的是输入能力 / 控制方式与镜头拆分方式（全能模式 / 首尾帧 / 行为起始帧 / Multi-Shot 等），本库解决的是电影语言里的镜头组织形式（单镜头 / master shot / shot-reverse-shot / insert / reaction / POV / montage 等）。

---

## 一、教材级总原则

- 先决定这场戏需要怎样的“观看关系”，再决定镜头怎么写。
- 先有镜头组织形式，再有单条 prompt。
- 一个场景不一定只靠一个镜头完成，很多“电影感”来自 coverage 的组合，而不是单条 prompt 写得更长。

---

## 二、常见镜头组织形式

### Pattern 命名规则（供 planner / storyboard 内部使用）

| Pattern ID | 名称 | 默认展开 |
|-----------|------|---------|
| `OBS_TENSION` | Observation Tension Coverage | `Shot 1` 建立观察关系 -> `Shot 2` 推进压迫 / 反应 |
| `CHASE` | Chase Coverage | `Shot 1` 跟拍建立速度 -> `Shot 2` 切新角度强化风险 |
| `PRESSURE_DIALOGUE` | Pressure Dialogue Coverage | `Shot 1` two-shot 建立关系 -> `Shot 2+` 单人/反应交替 |
| `INSERT_REACTION` | Insert + Reaction Coverage | `Shot 1` 关键物件或动作细节 -> `Shot 2` 人物反应 |
| `POV_REACTION` | POV + Reaction Coverage | `Shot 1` 主观看见 -> `Shot 2` 反应 |
| `REVEAL` | Reveal Coverage | `Shot 1` 等待或铺垫 -> `Shot 2` 揭示 -> `Shot 3` 反应（可选） |
| `MONTAGE` | Montage Pattern | 多个短镜头并置，不追求单条 prompt 完整性 |
| `MASTER_COVERAGE` | Master + Coverage | `Shot 1` master shot -> `Shot 2+` 近景/反应/insert |
| `OBJECT_SHOCK_REACTION` | Object Shock Reaction Coverage | `Shot 1` 小型关键物建立信息位 -> `Shot 2` 人物认出后的情感重击反应 |
| `ACTION_BRIDGE` | Action Bridge Coverage | `Shot 1` 起始机制/空间关系 -> `Shot 2` 身体动作链 -> `Shot 3` 受力/接续/结果 |
| `MECHANISM_CUTAWAY` | Mechanism Cutaway Coverage | `Shot 1` 入口/外部关系 -> `Shot 2` 侧剖面或 cutaway 交代内部机制 -> `Shot 3` 回到人物反应/职责关系 |

### Guardrail Profile 命名规则（仅供高频易错 Beat 触发）

> 用途：不是给所有 Beat 增加一层新系统，而是只给最容易反复踩坑的高频拍法补一组“命中即激活”的专属硬约束。
> 触发原则：只有当 Beat 的戏剧成立明显依赖这类关系时，`planner` 才应写入 `guardrail_profile`；未命中时保持为空。

| Guardrail Profile | 适用情形 | 默认依托 Pattern |
|------------------|---------|------------------|
| `TURN_CONFIRM_REVEAL` | 背后异动、回头确认、先画外后看见、转向后才确认危险 | `REVEAL` / `OBS_TENSION` / `POV_REACTION` |
| `OBJECT_SHOCK_REACTION` | 先见关键小物，再被“认出来”击中 | `OBJECT_SHOCK_REACTION` / `INSERT_REACTION` |
| `GROUP_PRESSURE_DIALOGUE` | 群像里有人把话顶给某人，靠权力关系与异步反应成立 | `PRESSURE_DIALOGUE` / `MASTER_COVERAGE` |
| `VERTICAL_DESCENT_MECHANISM` | 竖井、盗洞、下水道、深洞下行；观众必须看懂绳降、支点、守绳、深度关系 | `ACTION_BRIDGE` / `MECHANISM_CUTAWAY` |

### 1. 单镜头 / Sequence Shot / Oner

- 定义：
  - 一个连续镜头完成一段动作或情绪，不依赖切镜头。
- 教材启发：
  - 适合维持空间完整性、压迫等待感、强调 blocking 和真实时间流动。
- 最适合：
  - 守洞口、人物听动静、单人情绪压抑、空镜、简单动作
- 不适合：
  - 同时要交代关系、表情、空间变化、节奏转折的复杂段落
- 对 AI 漫剧的用法：
  - 适合简单镜头和稳定镜头
  - 如果连续两次都只生成“人物微动 + 轻推”，应切换到 coverage 或 Multi-Shot

### 2. Master Shot + Coverage

- 定义：
  - 先用一个主镜头覆盖整场戏，再用更近的镜头补反应、表情、细节。
- 教材启发：
  - master shot 的功能是至少完整覆盖场景，避免剪辑断裂；coverage 让编辑有情绪和节奏空间。
- 最适合：
  - 对话场景
  - 多人物调度
  - 一场戏里既有关系又有表情变化
- 对 AI 漫剧的用法：
  - `Shot 1` 负责建立空间和人物关系
  - `Shot 2 / Shot 3` 负责反应、近景、细节
  - 对话戏、观察戏、压迫戏优先考虑这种组织方式
  - 内部 Pattern ID 可记为 `MASTER_COVERAGE`
  - 群像里不要把所有角色写成同步静止反应，应让主说话人承担主表演，其他角色各自只给 1~2 个异步微变化
  - 如为连续群像戏，`Shot 2 / Shot 3` 即使收近，也应保持 `Shot 1` 已建立的屏幕左右关系与轴线，不得为了“更有戏”偷偷绕轴

### 3. Two-Shot

- 定义：
  - 两个人同时在画面中的双人镜头，用来建立两者关系和空间轴线。
- 最适合：
  - 对话开始前的关系建立
  - 情感连接
  - 权力对比
- 对 AI 漫剧的用法：
  - 常用于 `Shot 1`
  - 后续再切到更近的单人镜头或反应镜头

### 4. Shot-Reverse-Shot

- 定义：
  - 对同一空间中的两个对象，从相反方向交替切换，维持连续对话或对视关系。
- 教材启发：
  - 这是 continuity editing 的基础手段，常用于对话场景。
- 最适合：
  - 对话
  - 对峙
  - 对视
- 对 AI 漫剧的用法：
  - 可拆成 `Shot 1: A 视角 -> Shot 2: B 视角`
  - 如果模型不稳定 dirty OTS，优先 clean OTS 或匹配单人镜头
  - 常作为 `PRESSURE_DIALOGUE` 的内部展开方式
  - 使用前必须先锁定：这句台词主要是说给谁听，而不是默认对镜头说

### 5. Reaction Shot

- 定义：
  - 动作或台词发生后，切到另一个角色的反应。
- 教材启发：
  - 很多情绪并不在“谁做了事”，而在“别人怎么反应”。
- 最适合：
  - 惊吓
  - 凝重对白
  - 权力变化
  - 恐怖反应
- 对 AI 漫剧的用法：
  - 恐怖和悬疑里应主动设计反应镜
  - 台词说完后的沉默，常比继续跟说话者更有力
  - 常作为 `OBS_TENSION`、`PRESSURE_DIALOGUE`、`REVEAL`、`POV_REACTION` 的后半段
  - 群像反应优先写成“被某个词 / 某个异常信号击中后的一下变化”，不要把 reaction 写成固定表情贴图
  - 反应镜里的目光分配也应有主次，不要让所有人整齐看向同一个说话人

### 6. Insert Shot

- 定义：
  - 聚焦主动作中的某个物件、细节或局部动作。
- 教材启发：
  - insert 能传递信息、强调情绪、做伏笔，也能打破对话的平直感。
- 最适合：
  - 手、眼睛、枪、帛片、断手、绳索、手机、信件、钥匙
- 对 AI 漫剧的用法：
  - 适合做道具母题
  - 适合让漫剧更像“设计过的镜头”
  - 应短、小、准，不承担整场戏
  - 内部 Pattern ID 可记为 `INSERT_REACTION` 的起点

### 7. Cutaway

- 定义：
  - 暂时离开主动作，切向环境、旁观者或另一个信息点。
- 最适合：
  - 暗示危险
  - 引入新信息
  - 强化主题
  - 给剪辑留口
- 对 AI 漫剧的用法：
  - 用于洞口黑暗、林地深处、远处异响来源、天空、风吹草动

### 8. POV + Reaction Pair

- 定义：
  - 先给角色看到的东西，再给角色自己的反应，或反过来。
- 教材启发：
  - POV 建立主观体验，reaction 建立心理结果。
- 最适合：
  - 偷看、奔跑、惊恐发现、主观异常
- 对 AI 漫剧的用法：
  - 适合恐怖和悬疑
  - 比单纯写“他很害怕”更有戏
  - 内部 Pattern ID 可记为 `POV_REACTION`

### 9. Montage / Fragment Sequence

- 定义：
  - 通过多个短镜头并置，压缩时间、强化情绪或表现碎片记忆。
- 最适合：
  - 回忆
  - 训练
  - 追逐
  - 时间流逝
  - 情绪爆发
- 对 AI 漫剧的用法：
  - 不适合拿单条 prompt 硬做
  - 更适合拆成多个短片段，在剪辑阶段拼接
  - 内部 Pattern ID 可记为 `MONTAGE`

### 10. Object Shock Reaction

- 定义：
  - 先让观众看见一个“小而关键”的线索物，再切到角色认出该物后被击中的反应。
- 教材启发：
  - 本质是 `insert + reaction` 的情感版变体，但重点不在物件展示，而在“认出来”的瞬间。
- 最适合：
  - 地上旧物
  - 身份线索
  - 遗落物
  - 一眼能触发人物情感塌陷的关键证据
- 对 AI 漫剧的用法：
  - 第一镜优先后侧三分之四或背侧关系镜，不要正面展示式摆拍
  - 关键物应只占前景小面积，不可变成巨物
  - 如关键物不出现，戏就不成立，则该物必须独立 `@`
  - 第二镜沿同一信息方向收 reaction，重点是“认出来后的短暂停住、呼吸乱掉、胸口或肩膀回缩”
  - 如物件语义高风控，优先改写为“关键旧物 / 身份指向物”，必要时把物件信息拆到静帧，视频主打 reaction
  - 内部 Pattern ID 记为 `OBJECT_SHOCK_REACTION`

### 11. Action Bridge

- 定义：
  - 把上一拍的关系、命令或准备态，翻译成下一拍能继承的身体动作结果。
- 最适合：
  - 分工后开始执行
  - 拿起/交接/放下关键物
  - 进入洞口、翻越障碍、摔倒、被拖拽、绳索受力
- 对 AI 漫剧的用法：
  - `Shot 1` 先锁定起始关系与机制入口
  - `Shot 2` 给可见身体动作链：手、脚、重心、道具受力
  - `Shot 3` 停在动作造成的新关系或下一拍起点
  - 不得只写“开始执行 / 顺势下去 / 自然过渡”
  - 内部 Pattern ID 记为 `ACTION_BRIDGE`

### 12. Mechanism Cutaway

- 定义：
  - 暂时离开外部观察机位，用侧剖面、局部 cutaway 或机制示意式镜头，让观众理解复杂空间和身体动作如何成立。
- 最适合：
  - 竖井下行
  - 下水道入口
  - 洞壁攀爬
  - 绳降、滑落、卡住、拉扯等需要解释力学的动作
- 对 AI 漫剧的用法：
  - 不是科普图，也不是全景展示洞内世界；它只承担“空间机制可读”
  - 侧剖面镜头可以只显示黑暗边缘、人物剪影、手脚支点、绳线张力
  - 如果洞内设定必须纯黑，剖面镜不得突然打亮洞底或展示洞内完整通道
  - 内部 Pattern ID 记为 `MECHANISM_CUTAWAY`

---

## 三、按场景类型选镜头组织

| 场景类型 | 首选组织方式 | 备选 |
|---------|-------------|------|
| 单人观察、听动静 | `OBS_TENSION` | `POV_REACTION` |
| 紧张对话 | `PRESSURE_DIALOGUE` | `MASTER_COVERAGE` |
| 奔跑追逐 | `CHASE` | 单镜头跟拍 |
| 恐怖揭示 | `REVEAL` | `POV_REACTION` |
| 关键物件揭示 | `INSERT_REACTION` | Cutaway |
| 认出关键旧物 / 情感重击 | `OBJECT_SHOCK_REACTION` | `INSERT_REACTION` |
| 复杂动作桥 / 进入洞口 / 绳降 | `ACTION_BRIDGE` | `MECHANISM_CUTAWAY` |
| 竖井、下水道、深洞机制解释 | `MECHANISM_CUTAWAY` | `ACTION_BRIDGE` |
| 情绪递进 | `MASTER_COVERAGE` | `OBS_TENSION` |
| 回忆 / 时间压缩 | `MONTAGE` | 片段化转场 |

---

## 四、对 AI 工作流的直接规则

### 1. 单镜头适用条件

- 只有一个主动作
- 只有一个主情绪
- 不需要完整对话 coverage
- 不需要同时交代关系和表情

### 2. 优先 Multi-Shot 的条件

- 奔跑 / 追逐
- 观察 -> 压迫
- 紧张对话
- 先建立再推进
- 先看环境再看人
- 先看人再看反应

### 3. 优先 Insert / Reaction 的条件

- 关键道具是剧情点
- 情绪真正落在反应上
- 需要打断一段太平的对话或动作
- 需要先看见小型关键物，再看人物认出后的情感重击

### 5. 对话 / 顶撞 coverage 的额外规则

- 对话戏先判断 `谁对谁说`，再判断 `怎么拍`。
- 如果一句台词本质是顶给某个角色听的：
  - 机位应服务这条交流关系
  - 不要把说话人摆成面对镜头的采访机位
- 群像对话里，其他角色不应齐刷刷盯着说话人：
  - 有人看说话人
  - 有人看被顶撞对象
  - 有人先看异常点 / 环境，再被台词击中
- `PRESSURE_DIALOGUE` 和 `MASTER_COVERAGE` 都应默认检查：
  - screen geography 是否保持
  - 轴线是否保持
  - eyeline 是否合理

### 6. Pattern 触发式 Guardrails

#### A. `TURN_CONFIRM_REVEAL`

- 只在以下情形触发：
  - 背后异动
  - 角色转向确认
  - reveal 成立依赖“先不看见，转过去后才看见”
- planner 必须写清：
  - `screen_blocking_facts` 中 `setup 区` 与 `reveal 区` 的明确分离
  - `shot_function_chain` 至少包含：异动/截停 -> 转向/确认 -> 延迟揭示 -> 关系回扣
- storyboard 必须落地：
  - `setup` 段只能交代角色原本面对的空间，并明确写出不能出现的 reveal 主锚点
  - 中段反应镜不得写成正面展示式 / 采访式人物亮相镜
  - 回头必须写成可见动作链，不得只写“回头看去”
  - `reveal` 段才第一次进入新空间，并让威胁只部分成立
- review 重点检查：
  - 是否提前泄露 reveal 区
  - 中段是否被偷换成正面展示镜
  - 结尾是否落到人与危险的关系，而不是只停在对象露脸

#### B. `OBJECT_SHOCK_REACTION`

- 只在以下情形触发：
  - 小型关键物件一出现就改变人物判断
  - 戏真正落在“认出来”的心理重击
- 在改编自小说、章节文、原始剧情稿时，还必须保留原文里的“承载关系事实”。
  - 承载关系事实：关键物不是抽象地漂在画面里，而是明确附着在某个载体、动作链或人物持有关系上。
  - 例如：勾在土耗子上、被角色抓在手里、从怀里掏出、落在脚边、挂在低枝上。
- planner 必须写清：
  - 哪个物件是关键叙事物
  - 该物件是否需要独立 `@`
  - 关键物与人物的固定空间关系：物在人物前方 / 侧前方 / 脚边 / 地面 / 低枝 / 怀中，距离大约多少
  - 关键物的承载关系事实：它附着在哪个东西上、是被哪个动作带到当前画面的；如果原文已明确，优先继承原文，不得只剩抽象构图词
  - 反应镜里的主要情绪后果
- storyboard 必须落地：
  - 第一镜优先是信息位 / 关系位，不要把关键物拍成巨物或贴满前景
  - 第一镜必须把“物在哪、人物在哪、人物怎么看它”写成当前画面事实
  - 第一镜还必须把“物是怎么到这里的”写成当前画面事实；如果设定是“断手仍勾在土耗子上，被老三低头看见”，不得偷换成来历不明的低位异物
  - 第二镜重点必须是“认出来后的停顿、呼吸乱掉、回缩、压住”
  - 第二镜必须继承第一镜已经定义的目光方向与空间轴线；如果第一镜是看前下方地面，第二镜不得漂成回头看 / 侧后看 / 抬头看
  - 不得把戏重新写成“单纯展示物件”
- review 重点检查：
  - 关键物是否被正确 `@`
  - 物件尺度是否失真
  - 第一镜是否真正交代了物与人的固定空间关系
  - 原文 / director_analysis / scenes 中已经明确的承载关系事实，是否被 planner 和 storyboard 完整保留
  - 第二镜目光方向是否继承第一镜，而不是为了展示表情漂成另一套朝向
  - 反应是否真正落在人物而不是继续展示物件

#### C. `GROUP_PRESSURE_DIALOGUE`

- 只在以下情形触发：
  - 群像里有人把一句话顶给某人
  - 戏的成立依赖主说话人、被顶对象、旁观者反应三者关系
- planner 必须写清：
  - `dialogue_address`
  - `eyeline_rule`
  - `camera_side_rule`
  - 群像 screen geography 与主次表演承担者
- storyboard 必须落地：
  - 先建立关系，再收压力核心
  - 主说话人不能对着镜头播报
  - 配角反应必须异步分配，不能齐刷刷一起盯说话人
- review 重点检查：
  - 是否真的拍成“话是冲谁说的”
  - 群像站位和轴线是否保持
  - 配角是否有被台词击中的微变化过程

#### D. `VERTICAL_DESCENT_MECHANISM`

- 只在以下情形触发：
  - 深洞 / 竖井 / 下水道入口下行
  - 戏剧成立依赖观众看懂“谁在下、谁守绳、绳如何受力、洞有多深”
  - 直接拍入口动作会被模型生成成扶洞沿、爬台阶、跳下去或站在洞边摆拍
- planner 必须写清：
  - 洞口是垂直深洞、斜坡、台阶还是横向入口；不得混用
  - 谁是地面控绳者，第一帧是否必须已经抓住尾绳
  - 绳线从谁手里到洞口再到谁身上，受力方向是什么
  - 下行者允许使用哪些支点：绳、洞壁、洞沿短暂过渡；不得长期只靠扶洞沿
  - 是否需要单独拆 Beat 或补 `MECHANISM_CUTAWAY`
- storyboard 必须落地：
  - 第一镜必须同时看见地面控绳者或明确说明控绳者在画外如何受力；如果老三守尾绳是本拍因果，第一帧就不能漏掉他
  - 下洞动作必须是绳降 / 贴壁下沉 / 脚找支点，不得拍成走台阶、宽洞口钻入、集体跳下或抓扶手轻松下
  - 如果仍要表现深度，至少一镜采用高俯角、侧面机制镜或侧剖面 cutaway
  - 洞内保持纯黑时，只允许边缘轮廓、绳线和身体剪影，不展示洞底、洞内灯光或完整脸
- review 重点检查：
  - 第一帧是否有控绳职责
  - 是否看懂深度和受力机制
  - 是否把老三误混入下洞队列
  - 是否把洞口误生成为台阶、斜坡、门洞或宽阔隧道

### 4. 优先 Montage 的条件

- 时间压缩
- 记忆碎片
- 强烈动作过程
- 情绪爆发而不要求时空连续

---

## 五、planner / storyboard 调用方式

- `planner`
  - 先决定每个 Beat 的镜头组织形式
  - 再决定生成模式
- `storyboard`
  - 先继承镜头组织形式
  - 再写具体的 `Shot 1 / Shot 2 / Shot 3`

不要反过来。

先决定：
- 这是单镜头、master+coverage、shot-reverse-shot、insert+reaction、还是 montage

再决定：
- 用全能模式、首尾帧、行为起始帧，还是 Multi-Shot
- 用单张行为起始帧还是分镜图

---

## 六、参考来源提示

本库综合了常见电影教学与影视制作资料中的共识：

- shot size / establishing shot / insert shot / POV
- master shot / coverage
- shot-reverse-shot / reaction shot
- 180 degree rule / continuity editing

这些原则优先作为“镜头组织框架”使用，而不是要求在 prompt 中逐条明说术语。
