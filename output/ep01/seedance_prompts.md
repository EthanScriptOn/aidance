# Seedance 视频提示词 · ep01《血尸》

## 渲染目标

- 目标渲染器：seedance
- 本文件说明：本文件直接从 `output/ep01/beat_facts.yaml` 渲染，不依赖 `shot_plan.md`

## Beat 1 · 血土钩子

### 技法推理
- dramatic_task：先让观众被异常物钩住，再进入人物戏。
- information_anchor：洛阳铲铲头上的深红褐渗出物。
- candidate_techniques：单镜头 insert；先空镜再切特写。
- chosen_technique：单镜头 insert。
- reject_reason：这一拍没有人物反应，先空镜会稀释钩子强度。
- continuity_anchor：首拍，只继承全片月光方向。
- axis_rule：新建异常物观察轴。
- findings_hit：关键叙事物必须 `@`；单一信息点适合单镜。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单镜头 insert
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：5s
- registry 素材引用：
  - 洛阳铲铲头 `assets/images/prop_洛阳铲铲头_main.png`
  - 镖子岭荒野土丘 `assets/images/scene_镖子岭土丘_main.png`
- 本次上传顺序：
  - @图片1 = 洛阳铲铲头
  - @图片2 = 镖子岭荒野土丘

### 单次请求直贴 prompt
```text
只做一个镜头。@图片1 洛阳铲铲头插在 @图片2 镖子岭荒野土丘 顶面的作业区黄土里，镜头极近特写，只看铲头、黄土和渗出的深红褐液体，不给任何人物。月光从画面右上方斜切下来，阴影压向左下，整幅画面只有渗出物带一点暖色，其余都是冷蓝白月光和深褐黄土。镜头基本不动，只让液体湿润地慢慢往外晕开，停在这个异常物上。
```

## Beat 2 · 老烟头定性

### 技法推理
- dramatic_task：建立四人围铲的权力关系，并让“血尸”判断压住空气。
- information_anchor：群像弧形关系和老烟头的定性。
- candidate_techniques：master + reaction；直接单人特写。
- chosen_technique：master + reaction。
- reject_reason：直接特写会丢掉四人围铲和老烟头高位关系。
- continuity_anchor：承接同一土丘和同一铲头异常。
- axis_rule：从异常物轴扩展成群像轴，但不翻左右。
- findings_hit：群像连续性必须写当前站位；对话必须写给谁听；群像反应要异步。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：8s
- registry 素材引用：
  - 老烟头 `assets/images/char_老烟头_main.png`
  - 大胡子 `assets/images/char_大胡子_main.png`
  - 老二·独眼二伢子 `assets/images/char_老二·独眼二伢子_main.png`
  - 老三 `assets/images/char_老三_main.png`
  - 镖子岭荒野土丘 `assets/images/scene_镖子岭土丘_main.png`
  - 洛阳铲铲头 `assets/images/prop_洛阳铲铲头_main.png`
  - 旱烟枪 `assets/images/prop_旱烟枪_main.png`
- 本次上传顺序：
  - @图片1 = 老烟头
  - @图片2 = 大胡子
  - @图片3 = 老二·独眼二伢子
  - @图片4 = 老三
  - @图片5 = 镖子岭荒野土丘
  - @图片6 = 洛阳铲铲头
  - @图片7 = 旱烟枪

### 单次请求直贴 prompt
```text
Shot 1：在 @图片5 镖子岭荒野土丘 顶面，四个人围着地上的 @图片6 洛阳铲铲头 形成松散半弧。@图片1 老烟头在画面中央偏右略高位，手里拿着 @图片7 旱烟枪；@图片3 老二在画面左前较低位；@图片2 大胡子在老二侧后；@图片4 老三在右后外围低位。镜头先把这组围铲关系和 @图片6 这个中心锚点看清。Shot 2：收近到 @图片1 老烟头偏侧中近景，他先轻敲 @图片7 旱烟枪，眼睑微微压紧，嘴角向下收住，下颌稳稳绷着，握烟枪的手腕只顿一下，再慢慢说出“下面是个血尸嘎”，不是吼，是压场。Shot 3：不换轴，回到同一侧看另外三人的异步反应，@图片3 老二先绷住一下、鼻翼轻张，@图片2 大胡子下颌收紧、眼皮压低，@图片4 老三嘴角慢慢收住、肩背也跟着缩紧，所有人都先被地上的 @图片6 异常土和老烟头的话压住。月光统一来自右上，人物脸都是半亮半暗，洞口此时还不是主体。
```

## Beat 3 · 老二硬顶

### 技法推理
- dramatic_task：把家族内部的不稳推上桌，同时保住前一拍群像轴线。
- information_anchor：老二顶上来的身体动作和老烟头不动声色的压回。
- candidate_techniques：pressure dialogue coverage；单镜头对骂。
- chosen_technique：pressure dialogue coverage。
- reject_reason：单镜头对骂会把群像压成摆拍，失去父子侧后关系。
- continuity_anchor：承接 beat 2 的四人弧形关系。
- axis_rule：严格保持同一侧，镜头只收近不换边。
- findings_hit：群像压力对话要写清谁对谁说；配角反应必须异步。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：8s
- registry 素材引用：
  - 老烟头 `assets/images/char_老烟头_main.png`
  - 大胡子 `assets/images/char_大胡子_main.png`
  - 老二·独眼二伢子 `assets/images/char_老二·独眼二伢子_main.png`
  - 老三 `assets/images/char_老三_main.png`
  - 镖子岭荒野土丘 `assets/images/scene_镖子岭土丘_main.png`
  - 洛阳铲铲头 `assets/images/prop_洛阳铲铲头_main.png`
  - 旱烟枪 `assets/images/prop_旱烟枪_main.png`
  - 匣子炮（毛瑟C96） `assets/images/prop_匣子炮_main.png`
- 本次上传顺序：
  - @图片1 = 老烟头
  - @图片2 = 大胡子
  - @图片3 = 老二·独眼二伢子
  - @图片4 = 老三
  - @图片5 = 镖子岭荒野土丘
  - @图片6 = 洛阳铲铲头
  - @图片7 = 旱烟枪
  - @图片8 = 匣子炮（毛瑟C96）

### 单次请求直贴 prompt
```text
Shot 1：在 @图片5 镖子岭荒野土丘 顶面，地上的 @图片6 洛阳铲铲头 仍是四人弧形关系的中心锚点。@图片1 老烟头稳在中央偏右高位，@图片3 老二从左前方半站起来顶上来，身体前压，腰边带着 @图片8 匣子炮；@图片2 大胡子仍在老二侧后；@图片4 老三缩在右后外围。Shot 2：保持这组左右关系，@图片3 老二冲着 @图片1 老烟头发狠说话，不是对镜头喊；他说话时眉头压低，鼻翼轻张，嘴角绷直，下巴往前顶，肩线也发紧。Shot 3：切回同一侧更近一点，@图片1 老烟头拿着 @图片7 旱烟枪，不起火，只冷冷把老二压回去；他眼皮半垂，嘴角更薄地下压，下颌稳住不抖，持烟枪的手只轻轻抬一点。Shot 4：马上让 @图片2 大胡子从老二侧后补骂，父子一前一后都被老烟头压着；大胡子骂出口时眼角瞪紧、上唇一提、腮帮绷起，身体从老二侧后前探半步，@图片4 老三只敢在外围偷看。月光仍从右上切脸，不换轴，不重排人物。
```

## Beat 4A · 分工落定

### 技法推理
- knowledge_trace：
  - 公共决策：`knowledge/ai_generation/generation_decision_library.md`，判定为事件型关系变化，采用 multi-shot coverage。
  - 模式手册：`knowledge/ai_generation/modes/omnipotent_mode.md`，按全能模式使用人物/场景/关键道具多图 `@` 锚定，不使用分镜图驱动字段。
  - 模型渲染：`knowledge/ai_generation/model_renderer_playbooks.md`，按 Seedance 顺序式故事板指令组织。
  - 实测经验：`knowledge/ai_generation/video_field_test_findings.md`，采用“当前站位事实、关键物必须 @、群像异步反应”；Beat04 分镜图实测经验只转译为动作桥，不引入图内人物指认/关键帧时间分配。
  - 摄影灯光：`output/ep01/cinematography.md`，继承右上冷月、低调曝光、洞内纯黑、人物冷白边缘光。
- dramatic_task：把争执落成执行分工，明确谁是后续入洞顺位、谁被留在地面守退路。
- information_anchor：洞口为新中心后的群像重排和土耗子尾端控制关系。
- shot_type：事件型关系变化，不是纯状态镜；4秒以上必须靠“群像重排 -> 点名定序 -> 尾端交接 -> 老三反应”成立。
- candidate_techniques：master coverage；insert + reaction；直接下洞。
- chosen_technique：MASTER_COVERAGE / GROUP_PRESSURE_DIALOGUE，单次请求内按 Shot 1-4 顺序执行。
- reject_reason：insert + reaction 会丢掉三名后续下洞者的前中后顺位；直接下洞会偷跑 beat 04B，并让老三等待缺少前置职责。
- continuity_anchor：承接 beat 3 同一群像轴，只把中心从铲头换成洞口。
- axis_rule：允许围绕洞口重排，但老烟头仍压在右侧主导位。
- visibility_contract：本拍只能看见洞口外地面、四名完整人物、土耗子从老二/洞口侧延到老三手里；洞内保持纯黑，不能出现下洞身位、洞内人物、手脚、台阶或横向隧道。
- attention_contract：老烟头看洞口与三名被点名者；大胡子看烟枪手势和洞口；老二看绳线与洞口，偶尔瞥老烟头；老三看老烟头手势和自己手里的绳尾，不看镜头，也不看洞内深处。
- findings_hit：群像连续性必须写当前站位事实；关键叙事物必须 `@`；对话必须写清说给谁听；群像反应要异步；Beat04 实测的动作桥经验仅转译为全能模式的顺序节点，不使用分镜图专属字段。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：10s
- registry 素材引用：
  - 老烟头 `assets/images/char_老烟头_main.png`
  - 大胡子 `assets/images/char_大胡子_main.png`
  - 老二·独眼二伢子 `assets/images/char_老二·独眼二伢子_main.png`
  - 老三 `assets/images/char_老三_main.png`
  - 盗洞口 `assets/images/scene_盗洞口_main.png`
  - 土耗子 `assets/images/prop_土耗子_main.png`
  - 旱烟枪 `assets/images/prop_旱烟枪_main.png`
  - 匣子炮（毛瑟C96） `assets/images/prop_匣子炮_main.png`
- 本次上传顺序：
  - @图片1 = 老烟头
  - @图片2 = 大胡子
  - @图片3 = 老二·独眼二伢子
  - @图片4 = 老三
  - @图片5 = 盗洞口
  - @图片6 = 土耗子
  - @图片7 = 旱烟枪
  - @图片8 = 匣子炮（毛瑟C96）

### 单次请求直贴 prompt
```text
使用 @图片1 锁定老烟头，@图片2 锁定大胡子，@图片3 锁定老二·独眼二伢子，@图片4 锁定老三，@图片5 锁定盗洞口空间，@图片6 锁定土耗子，@图片7 锁定旱烟枪，@图片8 锁定匣子炮。单次请求生成一段连续 9:16 竖屏视频，中国探险悬疑漫画风，低调夜景，不是分镜图驱动，不要把参考图当作静态幻灯片。

Shot 1：在 @图片5 盗洞口外的地面，用同侧全景建立当前站位。28-35mm 标准广角感，中到大景深，四个人、洞口、洞沿和绳线都清楚。@图片1 老烟头从右侧主导位走到洞口前缘，双脚仍在地表；@图片2 大胡子跟在他左后半步，形成第二顺位但还没有下洞；@图片3 老二留在更后一点的左侧或后侧，一手主带 @图片6 土耗子 前端，腰边或手边可见 @图片8 匣子炮，形成第三顺位但仍在地面；@图片4 老三被压到洞口外侧右后守位，双脚踩实地面，身体想跟上但被排除在队列外。洞口是垂直向下的纯黑圆洞，不是台阶、门洞、斜坡或横向隧道。洞内不出现任何人物、手脚、身位、灯光或底部。

Shot 2：保持同一侧空间关系，不翻左右，不把人物洗牌。@图片1 老烟头半侧身朝洞口，头和 @图片7 旱烟枪 回向众人，先点洞口，再点 @图片2 大胡子，再点 @图片3 老二，最后压到 @图片4 老三守位，把“老烟头在前、大胡子居中、老二带土耗子殿后、老三留地面守尾端”的分工说死。老烟头眼尾不抬，嘴角薄薄压住，手腕动作小但很硬；@图片2 大胡子向洞口前压半步但不抢第一位；@图片3 老二看绳线和洞口，肩线收紧，匣子炮只作为腰边旧枪细节，不抢主焦点；@图片4 老三抬眼看老烟头手势，又低头看绳尾，不对镜头说话。

Shot 3：让 @图片6 土耗子 成为职责线。土耗子前端仍在准备入洞的三人这一侧，由 @图片3 老二主带；尾端必须明确交到 @图片4 老三双手里。绳子从洞口/老二这一侧斜向老三守位延伸，右侧有极细冷白轮廓线，不能变成无主散绳，也不能丢失。老三双手攥住尾端，站在地面退路位置，只负责守洞口、听里面吆喝后往外拉；他不能半身探进洞口，不能进入老烟头、大胡子、老二的入洞顺位。

Shot 4：最后落到 @图片4 老三被留在守位上的关系结果。老三眼圈发热但不哭大，眼里只保留很小的冷白高光，嘴角抿紧，呼吸往胸口里一缩，肩膀僵住，手指重新调整并抓牢 @图片6 土耗子 尾端；@图片1 老烟头只短促安抚一下，不改分工。@图片2 大胡子和 @图片3 老二在后景仍停在地面队列里，不开始下洞。最后停在“分工已经定死，三名后续入洞者仍在地面待命，老三被单独钉在守绳位置”的执行临界点。

摄影灯光全程继承：月光从画面右上方约40度斜切，人物右脸和右肩有冷白边缘光，左脸和身体背光面压入大块暗部；洞口边沿只有冷灰黄窄亮边，洞内深处完全纯黑；背景土丘和灌木整体压暗，只保留右侧冷白轮廓；人物通过脸部小亮块、肩线和冷白边缘光从背景中分离。禁止正前方采访机位，禁止所有人整齐看镜头，禁止把老三排进下洞队列，禁止任何角色在本拍结束前开始下洞，禁止直接跳到地面只剩老三的结果态。
```

## Beat 4B · 下洞启动

### 技法推理
- dramatic_task：把上一拍抽象的顺位和守绳职责翻译成可信的肉身下洞动作。
- information_anchor：垂直盗洞口、抓绳借力的动作机制、老三手里的土耗子尾端。
- candidate_techniques：action bridge；直接跳到老三等待。
- chosen_technique：action bridge。
- reject_reason：直接跳到等待会让三人像瞬间消失进洞，观众看不懂他们怎么下去。
- continuity_anchor：承接 beat 4A 的同一洞口站位和土耗子交接。
- axis_rule：继承洞口同侧轴线，可短暂用高俯角补机制，但回到侧看时不翻左右。
- findings_hit：动作链必须完整可读；关键连续道具必须 `@`；垂直空间不能误生成台阶/隧道；Beat04B 实测第一帧必须让老三控绳职责成立，深洞下行不能主要靠扶洞沿，应改为绳降 / 贴壁下沉 / 脚找支点。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：6s
- registry 素材引用：
  - 老烟头 `assets/images/char_老烟头_main.png`
  - 大胡子 `assets/images/char_大胡子_main.png`
  - 老二·独眼二伢子 `assets/images/char_老二·独眼二伢子_main.png`
  - 老三 `assets/images/char_老三_main.png`
  - 盗洞口 `assets/images/scene_盗洞口_main.png`
  - 土耗子 `assets/images/prop_土耗子_main.png`
  - 匣子炮（毛瑟C96） `assets/images/prop_匣子炮_main.png`
- 本次上传顺序：
  - @图片1 = 老烟头
  - @图片2 = 大胡子
  - @图片3 = 老二·独眼二伢子
  - @图片4 = 老三
  - @图片5 = 盗洞口
  - @图片6 = 土耗子
  - @图片7 = 匣子炮（毛瑟C96）

### 单次请求直贴 prompt
```text
Shot 1：在 @图片5 盗洞口，用轻微高俯角或同侧全景先看清下洞机制和队列：24-35mm 广角到标准广角感，中到大景深，洞沿、手、脚、绳子和老三守位都必须保持可读。第一帧就必须看见 @图片4 老三在洞口外侧地面控绳，他双脚踩实，身体后倾一点，双手已经抓住 @图片6 土耗子尾端；绳子从老三手里斜向洞口，再连到准备下行的三人这一侧。洞口是垂直向下的深黑竖井，不是台阶、门洞、斜坡、浅坑或横向隧道。低调曝光，洞内作为负光区域接近纯黑；月光从画面右上方约40°斜切下来，洞口右上口沿有冷灰黄窄亮边，洞内深处完全纯黑；人物右肩和右脸边缘有冷白边缘光，左侧身体被洞口负光压暗。@图片1 老烟头在洞口前缘第一个准备绳降，@图片2 大胡子贴在他左后半步等待第二个接续，@图片3 老二在第三位，腰边带着 @图片7 匣子炮，手边带着土耗子前段；@图片4 老三不进入队列。必须一眼看懂“前三人要下，老三留上面控尾绳”。

Shot 2：切同侧更近的洞口动作镜。动作清晰优先，只允许轻微运动模糊，手、脚、绳子和洞壁支点不能糊到看不懂。@图片1 老烟头先蹲低或坐到洞沿，双手抓住 @图片6 土耗子借力，一只脚先探到内侧洞壁找支点，另一只脚仍短暂停在口沿；随后他不是扶洞沿轻松下去，而是用绳子承重、背和肩贴近洞壁，身体重心一点点垂直下沉。扶洞沿只允许作为入口起手动作，核心必须是绳降和贴壁下行。老烟头越接近洞口，脸和胸口越被黑暗吞没，只保留右肩、手背、鼻梁右缘的一点冷白边线；手抓绳、脚踩洞壁处要有深暗接触阴影。洞口下方几寸后立刻纯黑，不能看见洞内底部、台阶、灯光或洞内人物脸。动作要慢半拍，让观众看懂他是沿垂直竖井下去，不是突然掉下去。

Shot 3：保持同一侧空间关系。@图片2 大胡子等 @图片1 老烟头下出半个身位后才压近洞口准备接续，不能抢到第一位；@图片3 老二在后面稳住 @图片6 土耗子，第三个殿后，@图片7 匣子炮仍在他腰侧或手边。绳线必须从洞口经过，另一端仍延到画面外侧 @图片4 老三手里。

Shot 4：最后落到 @图片4 老三守尾端的桥接镜。老三双手放绳又攥住尾端，脚踩实地面没有往洞里迈，眼神看着三人一个接一个被黑洞吞下；老三脸部半明半暗，眼里只有小的冷白高光，肩线被月光勾住。绳子从他手里斜向洞口，绳子右侧有极细冷白轮廓线，轻微滑动后被他重新控制住。背景土丘和灌木整体压暗，洞口是画面最黑的形体。最后停在“三人开始下去，老三仍在地面抓着土耗子尾端”的临界状态。全程不要让老三进洞，不要把洞口改成台阶或隧道，不要直接跳到地面只剩老三已经等了很久。
```

## Beat 5 · 洞口等待

### 技法推理
- dramatic_task：把“地面只剩老三一个人”拍成真正的等待压迫。
- information_anchor：老三守绳和右侧纯黑洞口。
- candidate_techniques：OBS_TENSION；单镜头长等待。
- chosen_technique：OBS_TENSION。
- reject_reason：纯长等 4 秒会发呆，需要“喊话 -> 留空 -> 回应”关系。
- continuity_anchor：承接 beat 4 的守位，老三在左，洞口在右。
- axis_rule：严格保持左老三右洞口。
- findings_hit：4 秒状态镜要改成功能关系；洞口危险源必须藏住。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：8s
- registry 素材引用：
  - 老三 `assets/images/char_老三_main.png`
  - 盗洞口 `assets/images/scene_盗洞口_main.png`
  - 土耗子 `assets/images/prop_土耗子_main.png`
- 本次上传顺序：
  - @图片1 = 老三
  - @图片2 = 盗洞口
  - @图片3 = 土耗子

### 单次请求直贴 prompt
```text
Shot 1：在 @图片2 盗洞口，@图片1 老三守在画面左侧偏前，蹲或半跪抓着 @图片3 土耗子，绳子从他手里延到画面右侧纯黑洞口。镜头用后侧三分之四观察，不给正面播报机位。Shot 2：他朝洞里喊一声，画面继续不动，右侧黑洞和绳子一起悬在那里，先留出明显空白等待。Shot 3：几秒后才从洞下传来断续模糊回应，老三不再闹脾气，脸和肩背明显绷住，继续盯着右侧黑里。洞里不出现任何人或肢体，月光仍从右上方打下来。
```

## Beat 6 · 听见不对

### 技法推理
- dramatic_task：让看不见的东西正式进场，但仍不现形。
- information_anchor：老烟头画外压声和老三被声音钉住的反应。
- candidate_techniques：OBS_TENSION；直接切洞内解释。
- chosen_technique：OBS_TENSION。
- reject_reason：切洞内会泄掉恐怖来源。
- continuity_anchor：完全承接 beat 5 的守位和左右关系。
- axis_rule：不越轴，不下洞。
- findings_hit：洞口黑暗威胁镜要把危险源藏住；状态镜要改成功能关系。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：7s
- registry 素材引用：
  - 老三 `assets/images/char_老三_main.png`
  - 盗洞口 `assets/images/scene_盗洞口_main.png`
  - 土耗子 `assets/images/prop_土耗子_main.png`
- 本次上传顺序：
  - @图片1 = 老三
  - @图片2 = 盗洞口
  - @图片3 = 土耗子

### 单次请求直贴 prompt
```text
Shot 1：在 @图片2 盗洞口，同一地面侧视仍保持左人右洞结构，@图片1 老三守在左侧位置，抓着 @图片3 土耗子，右侧是纯黑洞口。先只听见洞下压低的一句“轻点声……听！有动静！”，画面不切回下面。Shot 2：老三立刻被钉住，肩背和握绳的手收得更紧，呼吸压住，眼神死盯右侧黑里。Shot 3：在这个固定地面视角里，让咯咯怪声从黑洞里爬出来，但画面里绝不出现任何可见声源、手臂或挂件，只让声音先打在人身上。
```

## Beat 7 · 老三拔河

### 技法推理
- dramatic_task：把听觉异常升级成真实的物理拉扯。
- information_anchor：老三完整的受力链和绳线反力。
- candidate_techniques：单一动作镜；动作 + 受力后果双节点。
- chosen_technique：动作 + 受力后果双节点。
- reject_reason：只拍拉绳会缺少“反被拖”和“绑腰顶住”的关键信息。
- continuity_anchor：承接 beat 6 左老三右洞口。
- axis_rule：不越轴。
- findings_hit：洞口危险源只见力量不见目标；动作链必须完整可读。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：8s
- registry 素材引用：
  - 老三 `assets/images/char_老三_main.png`
  - 盗洞口 `assets/images/scene_盗洞口_main.png`
  - 土耗子 `assets/images/prop_土耗子_main.png`
- 本次上传顺序：
  - @图片1 = 老三
  - @图片2 = 盗洞口
  - @图片3 = 土耗子

### 单次请求直贴 prompt
```text
Shot 1：在 @图片2 盗洞口，画外先砸上一句“三伢子，拉！”，@图片1 老三立刻猛拽 @图片3 土耗子，仍然在画面左侧向右发力。Shot 2：下一秒反力突然从洞里把他往右侧黑洞拖过去，他脚下打滑，身体被拽歪，但洞里仍然不可见。Shot 3：老三急中生智把绳子勒到自己腰上，整个人向后倒，用背、腰、双腿一起死顶，受力链从左侧身体一直拉到右侧洞口，镜头只拍地面上的力量对抗，不下洞，不见目标。
```

## Beat 8 · 枪响，绳松

### 技法推理
- dramatic_task：把洞内灾难的结果一次性抛上地面，并完成关键 ownership 转移。
- information_anchor：同一件土耗子 bundle 弹出时带上匣子炮和外侧模糊挂物。
- candidate_techniques：单一弹出镜；枪响 -> 命令 -> 绳松 -> bundle 弹出。
- chosen_technique：顺序 multi-shot。
- reject_reason：如果只给“弹出一个东西”，枪、挂物、土耗子关系会漂。
- continuity_anchor：承接 beat 7 的僵持受力线。
- axis_rule：左老三右洞口不变。
- findings_hit：关键叙事物必须 `@`；结果链不能用泛称代替。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：6s
- registry 素材引用：
  - 老三 `assets/images/char_老三_main.png`
  - 盗洞口 `assets/images/scene_盗洞口_main.png`
  - 土耗子 `assets/images/prop_土耗子_main.png`
  - 匣子炮（毛瑟C96） `assets/images/prop_匣子炮_main.png`
  - 老二断臂·握拳 `assets/images/prop_老二断臂_fist.png`
- 本次上传顺序：
  - @图片1 = 老三
  - @图片2 = 盗洞口
  - @图片3 = 土耗子
  - @图片4 = 匣子炮（毛瑟C96）
  - @图片5 = 老二断臂·握拳

### 单次请求直贴 prompt
```text
Shot 1：在 @图片2 盗洞口，@图片1 老三还被绷直的 @图片3 土耗子 勒住，身体在画面左侧向右吃力。先响一声洞下匣子炮，再立刻传上来一声“快跑”。Shot 2：随着这句命令，绳子突然松掉，@图片3 土耗子 从右侧洞口中心朝老三胸前猛弹出来。Shot 3：必须把它写成同一件 carried bundle，@图片4 匣子炮 和 异常挂物@图片5 都跟着 @图片3 一起被带上来，异常挂物@图片5 仍被铁勾勾在 bundle 外侧，但这一拍不要把它拍成正面展示物。Shot 4：@图片1 老三迎面接住这整件 bundle，抱到胸前，立刻转身就跑。
```

## Beat 9 · 断手揭示

### 技法推理
- dramatic_task：先认出关键物，再让老三被情感重击。
- information_anchor：土耗子上勾着的老二断臂。
- candidate_techniques：OBJECT_SHOCK_REACTION；正面摆物特写。
- chosen_technique：OBJECT_SHOCK_REACTION。
- reject_reason：正面摆物容易变展示图，缺少“认出来”这一下。
- continuity_anchor：承接 beat 8，同一 bundle 被老三抱进林地。
- axis_rule：新建林地观察轴，但保留左臂抱 bundle、右腰有枪。
- findings_hit：关键物必须 `@`；关键物只占前景小面积；第一镜避免正面平铺。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：7s
- registry 素材引用：
  - 老三 `assets/images/char_老三_main.png`
  - 荒野林地 `assets/images/scene_荒野林地_main.png`
  - 土耗子 `assets/images/prop_土耗子_main.png`
  - 老二断臂·握拳 `assets/images/prop_老二断臂_fist.png`
  - 匣子炮（毛瑟C96） `assets/images/prop_匣子炮_main.png`
- 本次上传顺序：
  - @图片1 = 老三
  - @图片2 = 荒野林地
  - @图片3 = 土耗子
  - @图片4 = 老二断臂·握拳
  - @图片5 = 匣子炮（毛瑟C96）

### 单次请求直贴 prompt
```text
Shot 1：在 @图片2 荒野林地，@图片1 老三跑远后终于停下，站在画面左侧偏中，胸口还抱着 @图片3 土耗子，不要正面摆物。@图片5 匣子炮 已经顺手别到他的右腰，只露出一点，不抢主焦点。Shot 2：他把怀里的 @图片3 拉到眼前，这时才看清铁勾外侧挂着 身份代价物@图片4，关键物只占前景小面积。Shot 3：沿同一信息方向收老三反应，他先僵住，眼睑绷死，嘴微张一下又立刻咬住，喉结跟着一顶，短促哭一下又硬压住，眼神从身份代价物@图片4 上挪不开。
```

## Beat 10 · 回头看见血红东西

### 技法推理
- dramatic_task：用转向确认把“想回去救人”截断成新的危险。
- information_anchor：左前 setup 区的老三和右后 reveal 区的血尸。
- candidate_techniques：REVEAL；一镜直接把人和怪都端出来。
- chosen_technique：REVEAL。
- reject_reason：一镜直出会抹掉回头动作的空间意义。
- continuity_anchor：承接 beat 9，左臂仍夹着土耗子和断臂，右腰有枪。
- axis_rule：setup 区和 reveal 区必须分离。
- findings_hit：转向确认类戏点必须拆成画外异动 -> 转向反应 -> 延迟揭示；setup 镜不能提前露 reveal 区。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：6s
- registry 素材引用：
  - 老三 `assets/images/char_老三_main.png`
  - 荒野林地 `assets/images/scene_荒野林地_main.png`
  - 土耗子 `assets/images/prop_土耗子_main.png`
  - 老二断臂·握拳 `assets/images/prop_老二断臂_fist.png`
  - 匣子炮（毛瑟C96） `assets/images/prop_匣子炮_main.png`
  - 血尸 `assets/images/char_血尸_main.png`
- 本次上传顺序：
  - @图片1 = 老三
  - @图片2 = 荒野林地
  - @图片3 = 土耗子
  - @图片4 = 老二断臂·握拳
  - @图片5 = 匣子炮（毛瑟C96）
  - @图片6 = 血尸

### 单次请求直贴 prompt
```text
Shot 1：在 @图片2 荒野林地，@图片1 老三停在画面左前 setup 区，左臂仍夹着 @图片3 土耗子 和勾在其上的 身份代价物@图片4，右腰别着 @图片5 匣子炮。此时他原本面朝撤离方向或土丘方向，画面里不要提前出现任何血尸。Shot 2：右后方画外突然有异动，老三先头部回拧，再带动肩线转过去，右手摸到枪。Shot 3：直到他转过去后，才让 @图片6 血尸 在画面右后深处树干间被第一次确认，它蹲伏在暗部，逆光，只给血红轮廓和直勾勾的凝视，不完整冲出来。最后停在老三和血尸进入同一对峙轴。
```

## Beat 11 · 匣子炮对峙

### 技法推理
- dramatic_task：给观众一个“枪好像能压住它”的短暂假答案。
- information_anchor：老三右手持枪、血尸前扑、受击后仰。
- candidate_techniques：动作单镜；动作 + 后果双节点。
- chosen_technique：动作 + 后果双节点。
- reject_reason：只拍开枪不拍怪物后仰，压制感不成立。
- continuity_anchor：承接 beat 10 的同一对峙轴。
- axis_rule：老三始终在左前，血尸始终在右前，不翻左右。
- findings_hit：动作链要清楚；关键附着关系不能丢。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：9s
- registry 素材引用：
  - 老三 `assets/images/char_老三_main.png`
  - 荒野林地 `assets/images/scene_荒野林地_main.png`
  - 土耗子 `assets/images/prop_土耗子_main.png`
  - 老二断臂·握拳 `assets/images/prop_老二断臂_fist.png`
  - 匣子炮（毛瑟C96） `assets/images/prop_匣子炮_main.png`
  - 血尸 `assets/images/char_血尸_main.png`
- 本次上传顺序：
  - @图片1 = 老三
  - @图片2 = 荒野林地
  - @图片3 = 土耗子
  - @图片4 = 老二断臂·握拳
  - @图片5 = 匣子炮（毛瑟C96）
  - @图片6 = 血尸

### 单次请求直贴 prompt
```text
Shot 1：在 @图片2 荒野林地 里，@图片1 老三留在画面左前位，左臂仍带着 @图片3 土耗子 和 身份代价物@图片4，右手举起 @图片5 匣子炮，朝画面右前的 @图片6 血尸 压过去。Shot 2：@图片6 血尸突然前扑，几乎贴近老三。Shot 3：@图片1 老三近距离连发，枪口暖闪短暂照亮脸和空气，@图片6 血尸 被打得胸口后仰退开几步，但仍留在右前这一边，不要换位到别处。整段动作必须看清持枪、后坐和怪物后仰的连续关系。
```

## Beat 12 · 枪卡壳

### 技法推理
- dramatic_task：把上一拍的短暂希望当场掐断，并交代后面奔命的因果。
- information_anchor：卡壳 insert 和弃枪转身。
- candidate_techniques：单一逃跑镜；INSERT_REACTION。
- chosen_technique：INSERT_REACTION。
- reject_reason：直接跑会丢掉枪为什么没了、为什么只能跑。
- continuity_anchor：承接 beat 11 的同一对峙轴。
- axis_rule：前半仍是对峙轴，后半脱离转入逃命。
- findings_hit：关键动作桥不能省；ownership 转移结果要写成既成事实。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：5s
- registry 素材引用：
  - 老三 `assets/images/char_老三_main.png`
  - 荒野林地 `assets/images/scene_荒野林地_main.png`
  - 土耗子 `assets/images/prop_土耗子_main.png`
  - 老二断臂·握拳 `assets/images/prop_老二断臂_fist.png`
  - 匣子炮（毛瑟C96） `assets/images/prop_匣子炮_main.png`
  - 血尸 `assets/images/char_血尸_main.png`
- 本次上传顺序：
  - @图片1 = 老三
  - @图片2 = 荒野林地
  - @图片3 = 土耗子
  - @图片4 = 老二断臂·握拳
  - @图片5 = 匣子炮（毛瑟C96）
  - @图片6 = 血尸

### 单次请求直贴 prompt
```text
Shot 1：在同一片 @图片2 荒野林地 里，@图片1 老三还在画面左前，想用 @图片5 匣子炮 补最后一枪，画面先给一个清楚的枪失效瞬间，扳机扣下去却卡死。Shot 2：他脸上那点刚冒出来的希望立刻断掉，抡起 @图片5 匣子炮 就朝右前的 @图片6 血尸 砸过去。Shot 3：从这一刻起枪不再跟着他，@图片1 老三只带着左臂夹着的 @图片3 土耗子 和 身份代价物@图片4 转身就跑，迅速脱离对峙轴。
```

## Beat 13 · 装死与踩踏

### 技法推理
- dramatic_task：把“绊倒 -> 撞树墩 -> 装死 -> 被踩”这条关键动作桥完整落成。
- information_anchor：树墩、脸撞击点、贴地装死和血尸上压。
- candidate_techniques：直接趴地结果镜；动作桥 multi-shot。
- chosen_technique：动作桥 multi-shot。
- reject_reason：如果不拍绊倒和撞树墩，后面趴地装死没有因果。
- continuity_anchor：承接 beat 12，老三已无枪，只带土耗子 bundle 逃命。
- axis_rule：允许重建贴地轴，但逃跑方向、树墩位置和血尸压入方向必须清楚。
- findings_hit：关键动作桥不能被压成背景事实。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：8s
- registry 素材引用：
  - 老三 `assets/images/char_老三_main.png`
  - 荒野林地 `assets/images/scene_荒野林地_main.png`
  - 土耗子 `assets/images/prop_土耗子_main.png`
  - 老二断臂·握拳 `assets/images/prop_老二断臂_fist.png`
  - 血尸 `assets/images/char_血尸_main.png`
- 本次上传顺序：
  - @图片1 = 老三
  - @图片2 = 荒野林地
  - @图片3 = 土耗子
  - @图片4 = 老二断臂·握拳
  - @图片5 = 血尸

### 单次请求直贴 prompt
```text
Shot 1：在 @图片2 荒野林地，@图片1 老三已经无枪，只带着 @图片3 土耗子 和勾在上面的 身份代价物@图片4 狂奔。必须先落成关键动作桥：他先被低矮树桩绊到，整个人失去平衡。 Shot 2：紧接着他整张脸狠狠撞到树墩上，然后狗吃屎一样摔趴在地。就在这一下，@图片3 土耗子 和 身份代价物@图片4 从他左侧滑脱，落到他前方偏右一臂距离的地面。Shot 3：老三不再起身，顺势贴地装死。Shot 4：@图片5 血尸 从他前上方压入，一脚踩过他的背，再继续往前走，不停下来补杀。镜头尽量贴地，让观众和老三一起等那只脚压下来。
```

## Beat 14 · 尸毒发作

### 技法推理
- dramatic_task：明确老三从这一拍起进入中毒末态，并保住前方偏右的物件关系。
- information_anchor：老三身体感知和模糊的贴地视野。
- candidate_techniques：POV_REACTION；单一静态趴地镜。
- chosen_technique：POV_REACTION。
- reject_reason：单一静态镜会发死，也不能体现状态切换。
- continuity_anchor：承接 beat 13，血尸已踩过去，土耗子和断臂留在前方偏右。
- axis_rule：沿用贴地轴，只允许感知层虚化。
- findings_hit：状态切换必须在首次生效拍落地。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：6s
- registry 素材引用：
  - 老三（中毒末态） `assets/images/char_老三_tired.png`
  - 荒野林地 `assets/images/scene_荒野林地_main.png`
  - 土耗子 `assets/images/prop_土耗子_main.png`
  - 老二断臂·握拳 `assets/images/prop_老二断臂_fist.png`
- 本次上传顺序：
  - @图片1 = 老三（中毒末态）
  - @图片2 = 荒野林地
  - @图片3 = 土耗子
  - @图片4 = 老二断臂·握拳

### 单次请求直贴 prompt
```text
Shot 1：在 @图片2 荒野林地 的贴地机位里，@图片1 老三 已经是中毒末态，趴在画面下部低位，背部被踩过后整个人发虚，呼吸乱而压抑。Shot 2：让中毒先落在身体感知上，视线边缘开始发灰发虚，喉间返甜，眼前发糊，但空间事实不变，@图片3 土耗子 和 身份代价物@图片4 仍在他前方偏右可够到的位置。Shot 3：最后落在他意识到自己中毒了，却还在强撑着判断前方。
```

## Beat 15 · 帛片到手，第二张怪脸

### 技法推理
- dramatic_task：先完成人物最后的主动选择，再把更大的未知压下来。
- information_anchor：断手掌心里的古帛片，以及前上方压下来的第二实体怪脸。
- candidate_techniques：REVEAL；直接把帛片和怪脸一起端出来。
- chosen_technique：REVEAL，分前后两段。
- reject_reason：如果同时泄露地面取物和上方怪脸，人物选择会被怪脸吃掉。
- continuity_anchor：承接 beat 14，老三仍趴地，中毒末态，土耗子和断手在前方偏右。
- axis_rule：前半保持贴地取物轴，后半转成向上压迫轴。
- findings_hit：关键叙事物必须 `@`；转向/揭示类要分开 setup 和 reveal；组合物不要重复编号。
- target_renderer：seedance
- facts_check：已对齐

### 生成执行信息
- 目标渲染器：seedance
- 建议模型：Seedance 2.0
- 建议模式：全能模式，单次请求 multi-shot
- 屏幕尺寸：9:16
- 分辨率：1080x1920
- 视频建议时长：10s
- registry 素材引用：
  - 老三（中毒末态） `assets/images/char_老三_tired.png`
  - 荒野林地 `assets/images/scene_荒野林地_main.png`
  - 土耗子 `assets/images/prop_土耗子_main.png`
  - 老二断臂·握帛片 `assets/images/prop_老二断臂_cloth.png`
  - 第二实体 / 无瞳怪脸 `assets/images/char_第二实体怪脸_partial.png`
- 本次上传顺序：
  - @图片1 = 老三（中毒末态）
  - @图片2 = 荒野林地
  - @图片3 = 土耗子
  - @图片4 = 老二断臂·握帛片
  - @图片5 = 第二实体 / 无瞳怪脸

### 单次请求直贴 prompt
```text
Shot 1：在 @图片2 荒野林地，@图片1 老三 仍趴在画面下部低位，中毒发虚。他朝前方偏右拖身，那里有落地的 @图片3 土耗子 和 握帛片的身份代价物@图片4。先不要出现第二实体。Shot 2：镜头落到地面取物区，古帛片作为 握帛片的身份代价物@图片4 这个组合物的一部分，从掌心里露出来；老三艰难地掰开手指，把那片古帛从掌心里抠出来。Shot 3：必须明确落成那片古帛被塞进老三袖子，这一转移要看得见，但不要再给它单独第二个图片编号。Shot 4：耳鸣里咯咯声重新逼近，老三勉强抬头，这时才让 @图片5 第二实体 / 无瞳怪脸 从前上方或正上方压进画面，只给怪脸局部和没有瞳孔的空眼，不给完整身形，不做平视对峙。最后停在怪脸压下来的关系上。
```
