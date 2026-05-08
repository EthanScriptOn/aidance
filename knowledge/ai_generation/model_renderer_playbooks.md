# 模型渲染手册

本文件只解决一件事：

- `output/ep01/beat_facts.yaml` 是逐 Beat 的唯一事实锚点
- `output/ep01/shot_plan.md` 是可选的、模型无关的执行镜头卡
- 真正交给视频模型的提示词，必须按目标模型家族分别渲染

当前支持的渲染目标：

- `output/ep01/kling_prompts.md`
- `output/ep01/seedance_prompts.md`
- `output/ep01/storyboard_frame_prompts.md`
- `output/ep01/seedance_storyboard_prompts.md`

---

## 一、通用原则

1. 主链默认是 `beat_facts.yaml -> *_prompts.md`
2. 如存在 `shot_plan.md`，它不写模型私有语法，只负责辅助定义：
   - dramatic task
   - coverage pattern
   - shot function chain
   - continuity / blocking / eyeline / dialogue address
   - 建议生成策略与风险
3. `beat_facts.yaml` 是逐 Beat 的唯一事实源，负责定义：
   - 故事因果
   - blocking / axis / 距离 / 中心锚点
   - 关键物承载关系与 ownership 转移
   - 状态切换
   - 必须落成与不得违反的 shot contract
4. `*_prompts.md` 才负责：
   - 对应模型的输入能力选择
   - 对应模型更易读的 prompt 组织方式
   - 对应模型可执行的上传顺序与最终单次请求文案
5. `storyboard_frame_prompts.md` 只在高风险 Beat 启用：
   - 它是 `beat_facts.yaml` 与 `seedance_storyboard_prompts.md` 之间的唯一中间层
   - 每个 Beat 只允许 `2~4` 张关键帧
   - 每张关键帧必须已经是可直接用于生图的 prompt
   - 不再扩展成新的事实源
6. 一个 Beat 仍然只交付一条最终可请求 prompt。
   - 即使内部是 multi-shot，也必须合并成一条单次请求文案
7. 先定故事事实，再定电影技法，再定模型写法。
   - 如存在 `shot_plan.md`，不允许因为模型不同，就把其中镜头功能链改没了
   - 也不允许因为渲染器偏好，就把 `beat_facts.yaml` 里的关键事实改写成另一件事

---

## 二、渲染目标选择规则

### 1. Kling 渲染器

输出文件：

- `output/ep01/kling_prompts.md`

适用场景：

- 用户明确说要用可灵
- 用户明确说要用可灵 `omni`
- 当前测试目标是可灵的全能模式 / 首尾帧 / 多镜头能力

### 2. Seedance 渲染器

输出文件：

- `output/ep01/seedance_prompts.md`
- `output/ep01/storyboard_frame_prompts.md`
- `output/ep01/seedance_storyboard_prompts.md`

适用场景：

- 用户明确说要用 Seedance
- 当前测试目标是 Seedance 2.0 的多模态输入、分镜稿理解、图片混合引用能力

### 3. 未明确模型时

- 不得擅自把 `prompt` 阶段等同于 `kling`
- 先确认用户当前要测试的模型家族
- 如果用户未说明，但当前上下文已经明确在测某一模型，则沿用该模型家族

---

## 三、官方资料与能力锚点

### A. Kling 官方锚点

官方来源：

- Kling 官方 Prompt Guide：
  - https://kling.ai/blog/kling-ai-prompt-guide
- Kling VIDEO 3.0 官方 User Guide：
  - https://app.klingai.com/cn/quickstart/klingai-video-3-model-user-guide

从官方资料可直接确认的能力点：

- 支持文本到视频与图生视频
- 官方建议 prompt 以主体、动作、场景、镜头、光线/氛围等维度组织
- 支持 `Elements / Multi-Elements` 参考
- 支持 `Start and End Frames`
- 支持 `Multi-Shot` / `Custom Multi-Shot`

因此 Kling 渲染时：

- 可以显式写 `Shot 1 / Shot 2 / Shot 3`
- 可以在同一条 prompt 中组织多镜头递进
- 可以明确交付：
  - 全能模式（图生视频）
  - 首尾帧（图生视频）
  - 单张行为起始帧（图生视频）
  - Multi-Shot（单次请求）

### B. Seedance 官方锚点

官方来源：

- Seedance 官方产品页：
  - https://seed.bytedance.com/seedance
- Seedance 2.0 官方发布说明：
  - https://seed.bytedance.com/blog/seedance-2-0-official-launch
- Seedance 2.0 官方英文页：
  - https://seed.bytedance.com/en/seedance2_0

从官方资料可直接确认的能力点：

- 支持 text / image / audio / video 混合输入
- 支持最多 9 张图片输入
- 官方示例明确说明可直接理解带 `@Image` 的分镜稿或故事板式输入

说明：

- Seedance 官方公开资料里，关于“提示词 cookbook”的细致程度弱于 Kling
- 因此本手册里对 Seedance 的写法约束，部分来自官方能力说明，部分来自基于官方示例的保守推断
- 这类推断必须始终服务于 `beat_facts.yaml` 主源；如存在 `shot_plan.md`，也只能辅助，不得反过来改写叙事任务

因此 Seedance 渲染时：

- 优先采用分镜稿式、顺序式、场面调度清楚的表达
- 优先显式写清镜头顺序与画面允许/禁止出现的内容
- 优先利用图片锚点、角色锚点、场景锚点，而不是堆很多抽象风格词
- 如为多镜头结构，优先写成顺序分段：
  - `Shot 1 ... Shot 2 ... Shot 3 ...`
  - 或 `先……随后……这时才……最后……`
- 如某个 Beat 已明确启用分镜图驱动：
  - 先生成 `storyboard_frame_prompts.md`
  - 再使用 `seedance_storyboard_prompts.md`
  - 让 `@图片1 @图片2 @图片3` 对应 `storyboard_frame_prompts.md` 中的关键帧成品图
  - 适合 setup / reveal / reaction / payoff 节点非常清楚、且纯文本全能模式容易漂移的 Beat
  - 但关键帧只能作为构图锚点，不能把最终 prompt 写成“前几秒看 @图片1，中间几秒看 @图片2，最后几秒看 @图片3”
  - 每个关键帧节点都必须补清楚动作桥：谁先动、身体哪个部位动、道具或空间关系怎样变化、最后落到哪张关键帧的关系
  - 具体规则以 `knowledge/ai_generation/modes/storyboard_frame_mode.md` 为准

## 选择规则

某个 Beat 该走哪种模式，默认按以下最简判定：

- `全能模式`
  - 单镜头 insert
  - 普通 reaction
  - 简单 two-shot
  - 群像关系不复杂，且之前未发生明显漂移

- `首尾帧`
  - 起始构图和结束构图非常明确
  - 中间只需要有限变化
  - 同一镜头内部完成推进

- `全能模式 + multi-shot`
  - 需要 2~3 个镜头节点
  - 但不值得为它单独先做分镜图

- `分镜图驱动`
  - 需要稳定落成 3 个以上关键节点
  - setup 区与 reveal 区强分离
  - 复杂群像站位一旦漂移就没法用
  - 关键动作桥丢了就看不懂因果

---

## 四、Kling 渲染规则

1. 优先短句、明确动作、明确镜头顺序
2. 如使用全能模式：
   - 正文默认采用 `对象名@图片X` 写法
   - 图片承担静态锚点，正文承担动作、表情、镜头关系
3. 如存在 `shot_plan.md` 且其中明确为 multi-shot：
   - 允许显式 `Shot 1 / Shot 2 / Shot 3`
   - 但最终仍必须合并成一条单次请求 prompt
4. 如存在 `shot_plan.md` 且其中明确为首尾帧：
   - 必须把起始帧、结束帧、过渡目标写清
5. 台词处理：
   - 可把台词直接写在 prompt 里
   - 如当前流程明确要利用可灵声音能力，可额外建议用户开启相应声音能力
6. 少写泛化风格词，多写：
   - 屏幕站位
   - 动作变化
   - 反应信号
   - reveal 约束

---

## 五、Seedance 渲染规则

1. 优先把镜头理解成“故事板指令”，而不是风格词堆砌
2. 更强调：
   - 谁在图几
   - 谁位于画面哪一侧
   - 先出现什么
   - 后出现什么
   - 哪块空间必须暂时不出现
3. 如为多镜头结构：
   - 优先显式写顺序节点
   - 不要把多镜头压成一整段抽象总结
   - 默认优先采用故事板式写法：
     - `Shot 1 / Shot 2 / Shot 3`
     - 或“先……随后……这时才……最后……”这类等价顺序写法
   - 让模型先读懂镜头顺序、动作顺序和结果顺序，再读情绪与氛围
4. 优先让图片承担角色与场景锚点：
   - 人物图锚定身份
   - 场景图锚定空间
   - 道具图锚定关键叙事物
5. 台词处理：
   - 如官方未明确对应能力，不默认承诺“模型自动带口型与声音”
   - 仍可把台词作为表演意图写进 prompt，但不要把模型未确认的能力当硬规则
6. 尽量减少无效修辞，优先保留：
   - shot function chain
   - blocking facts
   - eyeline / dialogue address
   - 允许出现 / 禁止出现
   - 可执行的镜头事实：
     - 谁站在哪
     - 谁先动
     - 镜头先看哪
     - 哪个物件何时进入
     - 画面最后停在哪里
7. 少写抽象风格词，多写导演指令式的可执行事实。
   - 不要只写“阴森、电影感、压迫、史诗、紧张”这类抽象修辞而缺少动作链。
   - 对 Seedance，优先把 prompt 写成可拍摄的故事板指令：
     - 主体是谁
     - 当前构图关系是什么
     - 动作如何推进
     - 镜头如何切换或跟进
     - 最后落到什么后果或关系
8. 不得在渲染层抹平上游已经定义的剧情事实。
   - 尤其是关键物的来源、承载关系、与人物的固定空间关系。
   - 如果 `beat_facts.yaml` 或可选 `shot_plan.md` 已明确“物挂在什么上、从哪里被看见、由谁拿着”，最终 prompt 不得改写成更模糊的 `hanging`、`resting low in frame`、`nearby object` 这类抽象说法。
9. 下游渲染前，必须先做 facts mapping：
   - 每个 Beat 至少检查一次 `story_facts`
   - 每个 Beat 至少检查一次 `blocking_facts`
   - 每个 Beat 至少检查一次 `object_continuity`
   - 每个 Beat 至少检查一次 `shot_contract`
10. 当上游对关键物关系写得不够死时，不允许擅自脑补成泛化安全描述，应先回溯补全上游。
   - 优先回查 `director_analysis.md`
   - 优先回查 `beat_facts.yaml`
   - 再回查 `assets/scenes.md`
   - 如任务本身来自小说 / 章节文 / 剧情稿，再回查原始文本
   - 只有当“关键物在哪、附着在什么上、人物如何发现它”都明确后，才进入最终渲染 prompt

---

## 六、渲染产物固定格式

无论是 Kling 还是 Seedance，最终 Beat 级交付必须包含：

1. `技法推理`
2. `目标渲染器`
3. `建议模型`
4. `建议模式`
5. `屏幕尺寸`
6. `分辨率`
7. `视频建议时长`
8. `registry 素材引用`
9. `本次上传顺序`
10. `单次请求直贴 prompt`

如目标文件是 `seedance_storyboard_prompts.md`，还必须补充：

11. `关键帧时间分配`
12. `台词策略`
13. `图内人物指认`
14. `动作桥检查`

补充说明：

- `seedance_storyboard_prompts.md` 不是“关键帧桥接说明”，而是最终执行单
- 必须告诉用户每张关键帧大致承担哪段时间职责
- 关键帧时间分配只能写“承担的镜头功能”，不能写成静态停留时长；例如写“@图片1 作为起始 master 构图，人物开始重排”，不要写“@图片1 约 3 秒”
- 如果只上传成品分镜图、不再上传单独角色图，必须补 `图内人物指认`，用图中可见外貌、位置和职责把角色名绑定清楚
- 单次请求 prompt 必须显式避免幻灯片式输出：要求生成连续视频动作和可见表演，不要把三张图当作静态画面依次播放
- 每个关键帧节点至少要有一个可见动作动词；如果某节点没有动作，只承担构图展示，必须改成更短的建立镜或改用别的生成策略
- 必须判断台词走哪条路径：
  - 无台词
  - 仅表演意图，不要求口型
  - 需说出台词
  - 交给后期配音

补充要求：

- `目标渲染器` 只能写当前这一份产物实际对应的模型家族
- `建议模型` 是该渲染器内的具体模型建议
- `建议模式` 必须写成用户可以直接执行的口径
- 同一份文件内不要混写两套不同模型的最终 prompt

---

## 七、下游阶段依赖

- `edit`
- `sound`
- `post`

默认不再写死依赖 `kling_prompts.md`。

它们应依赖：

- 当前已生成、且用户准备真正拿去生视频的 prompt 产物
- 即：
  - `kling_prompts.md`
  - 或 `seedance_prompts.md`

如果两个文件都存在：

- 必须先确认本轮视频生成实际采用的是哪一份
- 不得混读后再输出一份自相矛盾的后续方案
