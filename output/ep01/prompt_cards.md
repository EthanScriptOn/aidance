# Prompt Cards · ep01

> 使用说明：本文件是可测试提示词卡。凡标注“正式阻塞”的 Clip，应先按 `asset_manifest.md` 和 `asset_regen_plan.md` 补齐资产；若做冷启动临时测试，可上传现有 新流程待跑图，但测试结果不能回写为正式结论。

## Clip 01 · 铲头渗液

事实卡：

```text
原文范围：开头至“都要撂在下面噢。”
可见人物：老烟头、大胡子、老二、老三
需要参考图：assets/images/scenes/scene_镖子岭土丘_shovel_area.png；assets/images/props/prop_洛阳铲铲头_identity.png；assets/images/characters/char_老烟头_identity.png；assets/images/characters/char_大胡子_identity.png；assets/images/characters/char_老二_identity.png；assets/images/characters/char_老三_identity.png；assets/images/props/prop_旱烟枪_identity.png
地点：长沙镖子岭土丘顶面，夏夜月光
关键道具：洛阳铲铲头、旱烟枪
开始状态：四人沉默盯着铲头。
结束状态：老烟头确认下面有血尸，取得解释权。
不可错事实：铲头渗出的是深红褐湿痕；四人还在地面；洞内不亮。
```

戏剧卡：

```text
主要欲望：四人想判断地底情况。
阻力：铲头上的异常湿痕说明经验之外的危险。
状态变化：沉默观察 -> 被老烟头一句话定性为大麻烦。
观众感受：第一眼就知道这趟买卖不干净。
行为链：围铲沉默；湿痕渗出；少年紧张；老烟头敲烟枪；大胡子看洞口；老烟头开口；众人被压住。
```

提示词卡：

```text
建议模型：Seedance 2.0
建议模式：image-to-video，多图参考
画幅：9:16
时长：6 秒
镜头数：7

上传顺序：
@图片1 = assets/images/scenes/scene_镖子岭土丘_shovel_area.png
@图片2 = assets/images/props/prop_洛阳铲铲头_identity.png
@图片3 = assets/images/characters/char_老烟头_identity.png
@图片4 = assets/images/characters/char_大胡子_identity.png
@图片5 = assets/images/characters/char_老二_identity.png
@图片6 = assets/images/characters/char_老三_identity.png
@图片7 = assets/images/props/prop_旱烟枪_identity.png

直贴提示词：
使用 @图片1 锁定土丘顶面夜景，@图片2 锁定洛阳铲铲头，@图片3-6 锁定四个土夫子，@图片7 锁定旱烟枪。生成 9:16 竖屏视频，约 6 秒，7 个快速镜头。核心情绪：地底危险第一次被看见。
Shot 1，中远景，0.8秒：四人蹲成松散弧形，全部盯着地上的洛阳铲。
Shot 2，极近特写，0.7秒：铲头旧土里缓慢渗出深红褐湿痕。
Shot 3，近景，0.7秒：老三眼睛一缩，老二硬撑着不后退。
Shot 4，中近景，0.8秒：老烟头用旱烟枪敲地，众人视线转向他。
Shot 5，反应近景，0.7秒：大胡子下意识看向黑洞方向。
Shot 6，老烟头近景，0.8秒：老烟头低声说“麻烦大喽”，脸色沉下。
Shot 7，关系全景，1.5秒：四人围着铲头停住，老烟头成为唯一发话的人。
灯光：冷蓝白月光从右上方切入，洞口保持纯黑。
表演：少说话，用视线、停顿和手部动作表达判断。
禁止：不要出现现代物品，不要让洞内发光，不要增加其他人物。
```

## Clip 02 · 老二顶嘴

事实卡：

```text
原文范围：“下不下去喃？”至“不是有只匣子炮就能喔荷西天。”
可见人物：老烟头、大胡子、老二、老三
需要参考图：assets/images/scenes/scene_镖子岭土丘_shovel_area.png；assets/images/characters/char_老烟头_identity.png；assets/images/characters/char_大胡子_identity.png；assets/images/characters/char_老二_identity.png；assets/images/characters/char_老三_identity.png；assets/images/props/prop_旱烟枪_identity.png
地点：土丘顶面，洛阳铲和盗洞附近
关键道具：旱烟枪，匣子炮可不出镜
开始状态：老二急着下去。
结束状态：老二被老烟头的经验压住。
不可错事实：老二是独眼小伙子；老烟头不是发怒，而是不怒反笑。
```

戏剧卡：

```text
主要欲望：老二想证明自己敢下洞。
阻力：老烟头把他的胆量定义成鲁莽。
状态变化：冲动挑战 -> 当众被削弱。
观众感受：这个年轻人会惹事。
行为链：老二半站；老烟头笑；大胡子沉脸；烟枪点人；老二僵住；老三偷看；老烟头压场。
```

提示词卡：

```text
建议模型：Seedance 2.0
建议模式：image-to-video，多图参考
画幅：9:16
时长：6 秒
镜头数：7

上传顺序：
@图片1 = assets/images/scenes/scene_镖子岭土丘_shovel_area.png
@图片2 = assets/images/characters/char_老烟头_identity.png
@图片3 = assets/images/characters/char_大胡子_identity.png
@图片4 = assets/images/characters/char_老二_identity.png
@图片5 = assets/images/characters/char_老三_identity.png
@图片6 = assets/images/props/prop_旱烟枪_identity.png

直贴提示词：
使用 @图片1 锁定土丘顶面，@图片2-5 锁定人物，@图片6 锁定旱烟枪。生成 9:16 竖屏视频，约 6 秒，7 个镜头。核心情绪：年轻人的冒进被老人压住。
Shot 1，中景，0.8秒：老二半站起来，身体前倾，独眼直顶老烟头。
Shot 2，老烟头近景，0.7秒：老烟头不怒反笑，慢慢转头看大胡子。
Shot 3，大胡子近景，0.7秒：大胡子脸沉下来，眼神压向老二。
Shot 4，中近景，0.8秒：老烟头抬旱烟枪点向老二，话锋压住他。
Shot 5，老二近景，0.7秒：老二嘴角一僵，刚才的冲劲断掉。
Shot 6，老三反应，0.7秒：老三蹲在边上偷看，紧张又羡慕。
Shot 7，关系全景，1.6秒：四人位置不变，但发言权落在老烟头身上。
灯光：冷月光右上方，人物半边脸在暗部。
表演：老二动作快，老烟头动作慢，权力差靠节奏表现。
禁止：不要让老二戴眼罩；不要把匣子炮夸张展示成现代枪。
```

## Clip 03 · 老三被排除

事实卡：

```text
原文范围：“等一下我先下去”至“你要再吆喝，我拧你个花麻鸡吧！”
可见人物：老烟头、大胡子、老二、老三
需要参考图：assets/images/scenes/scene_镖子岭土丘_shovel_area.png；assets/images/scenes/scene_盗洞口_action_area.png；assets/images/characters/char_老烟头_identity.png；assets/images/characters/char_大胡子_identity.png；assets/images/characters/char_老二_identity.png；assets/images/characters/char_老三_identity.png；assets/images/props/prop_土耗子_identity.png
地点：土丘顶面，盗洞口旁
关键道具：土耗子
开始状态：老三想下洞。
结束状态：老三被迫守绳。
不可错事实：老三是最小的；老二揪耳朵；大胡子没有救场。
```

戏剧卡：

```text
主要欲望：老三想证明自己能下洞。
阻力：老烟头分工、老二暴力、大胡子沉默。
状态变化：抗议 -> 被压服。
观众感受：守绳不是选择，是被关系推到的位置。
行为链：老烟头分配；老三抗议；老二揪耳；老三求救；大胡子转开；老二威胁；老三闭嘴握绳。
```

提示词卡：

```text
建议模型：Seedance 2.0
建议模式：image-to-video，多图参考
画幅：9:16
时长：6 秒
镜头数：7

上传顺序：
@图片1 = assets/images/scenes/scene_镖子岭土丘_shovel_area.png
@图片2 = assets/images/scenes/scene_盗洞口_action_area.png
@图片3 = assets/images/characters/char_老烟头_identity.png
@图片4 = assets/images/characters/char_大胡子_identity.png
@图片5 = assets/images/characters/char_老二_identity.png
@图片6 = assets/images/characters/char_老三_identity.png
@图片7 = assets/images/props/prop_土耗子_identity.png

直贴提示词：
使用 @图片1-2 锁定土丘与洞口关系，@图片3-6 锁定人物，@图片7 锁定土耗子。生成 9:16 竖屏视频，约 6 秒，7 个快镜头。核心情绪：老三被迫成为地面守绳人。
Shot 1，中景，0.8秒：老烟头指向洞口和土耗子，开始分配谁下去谁留在上面。
Shot 2，老三近景，0.7秒：老三撅嘴抗议，身体往洞口方向挤。
Shot 3，动作近景，0.7秒：老二一把揪住老三耳朵，把他拽回地面位置。
Shot 4，老三反应，0.7秒：老三痛得缩肩，眼睛看向大胡子求救。
Shot 5，大胡子中景，0.8秒：大胡子转身收拾家伙，没有看老三。
Shot 6，老二压迫近景，0.8秒：老二贴近威胁，老三不敢再吭声。
Shot 7，关系全景，1.5秒：土耗子尾巴落在老三手里，其他人朝洞口准备下去。
灯光：土丘顶面冷月光，洞口纯黑。
表演：老三从硬顶到收缩；老二动作粗暴但不要夸张滑稽。
禁止：不要让老三主动开心接受任务；不要增加旁观者。
```

## Clip 04 · 操家伙下洞

事实卡：

```text
原文范围：“小子们，操家伙啰！”至“盗洞已经打得见不到底了”
可见人物：老烟头、老二、大胡子、老三
需要参考图：assets/images/scenes/scene_盗洞口_action_area.png；assets/images/characters/char_老烟头_identity.png；assets/images/characters/char_大胡子_identity.png；assets/images/characters/char_老二_identity.png；assets/images/characters/char_老三_identity.png；assets/images/props/prop_土耗子_identity.png
地点：盗洞口
关键道具：土耗子、绳子、洞口
开始状态：四人还在地面。
结束状态：老三在地面，其他人被洞口吞没，绳子成为唯一联系。
不可错事实：老三没有下洞；洞里不可见。
```

戏剧卡：

```text
主要欲望：老烟头把争执转成行动。
阻力：盗洞深黑，进去后无法一起退。
状态变化：地面群体 -> 地上地下分离。
观众感受：危险开始离开视野。
行为链：号令；拿工具；递绳；人靠洞；老三握尾；身影消失；绳子垂黑。
```

提示词卡：

```text
建议模型：Seedance 2.0
建议模式：image-to-video，多图参考
画幅：9:16
时长：6 秒
镜头数：7

上传顺序：
@图片1 = assets/images/scenes/scene_盗洞口_action_area.png
@图片2 = assets/images/characters/char_老烟头_identity.png
@图片3 = assets/images/characters/char_大胡子_identity.png
@图片4 = assets/images/characters/char_老二_identity.png
@图片5 = assets/images/characters/char_老三_identity.png
@图片6 = assets/images/props/prop_土耗子_identity.png

直贴提示词：
使用 @图片1 锁定盗洞口，@图片2-5 锁定四人，@图片6 锁定土耗子。生成 9:16 竖屏视频，约 6 秒，7 个镜头。核心情绪：队伍分成洞里和地面。
Shot 1，中景，0.8秒：老烟头拍老二肩膀，大声发号施令。
Shot 2，动作近景，0.7秒：几只手快速抓起工具和土耗子。
Shot 3，中景，0.8秒：土耗子尾巴被放到老三手里。
Shot 4，俯视中景，0.7秒：老烟头、大胡子、老二依次靠近洞口。
Shot 5，老三近景，0.8秒：老三握紧绳尾，不甘心地看他们下去。
Shot 6，洞口特写，0.8秒：最后一个身影消失，绳子垂入纯黑。
Shot 7，关系落点，1.4秒：老三独自留在洞口边，手里只有绳尾。
灯光：月光照洞口边缘，洞内绝对黑。
表演：下洞动作果断，老三停在原地形成落差。
禁止：不要展示洞内空间；不要让四个人都下去。
```

## Clip 05 · 洞口喊话

事实卡：

```text
原文范围：“老三等得不耐烦起来”至“拉好……好绳子！”
可见人物：老三
需要参考图：assets/images/scenes/scene_盗洞口_action_area.png；assets/images/characters/char_老三_identity.png；assets/images/props/prop_土耗子_identity.png
地点：盗洞口
关键道具：土耗子绳尾
开始状态：老三无聊等待。
结束状态：老三确认洞下声音模糊，开始紧张守绳。
不可错事实：洞内人物不露面，只传来延迟声音。
```

戏剧卡：

```text
主要欲望：老三想知道洞里挖穿没有。
阻力：洞深、声音断续、回应延迟。
状态变化：不耐烦 -> 警觉。
观众感受：地面和洞下的联系正在变弱。
行为链：绕绳等待；喊话；黑洞沉默；探身听；模糊回应；抓紧绳；独自守洞。
```

提示词卡：

```text
事实：老三独自守在盗洞口，手握土耗子绳尾，朝洞里喊“大爷爷，挖穿没有？”，几秒后听见模糊回应“待在上面，拉好绳子”。
上传顺序：@图片1=assets/images/scenes/scene_盗洞口_action_area.png；@图片2=assets/images/characters/char_老三_identity.png；@图片3=assets/images/props/prop_土耗子_identity.png
Seedance 直贴提示词：
使用 @图片1 锁定盗洞口纯黑空间，@图片2 锁定老三，@图片3 锁定土耗子。生成 9:16 竖屏视频，约 6 秒，7 个镜头。核心情绪：等待变成失联。
Shot 1，中景，0.8秒：老三蹲在洞边，手指绕着绳尾。
Shot 2，近景，0.7秒：他朝洞里喊“大爷爷，挖穿没有？”
Shot 3，洞口特写，0.8秒：黑洞沉默几秒，只有绳子垂下。
Shot 4，老三近景，0.7秒：老三身体往前探，耳朵靠近洞口。
Shot 5，绳子近景，0.7秒：绳子轻轻颤一下，洞底传来断续模糊回应。
Shot 6，老三反应，0.8秒：他抓紧绳子，不耐烦消失。
Shot 7，全景，1.5秒：老三一个人守在洞口边，洞里仍然看不见任何东西。
灯光：冷月光打洞口边缘，洞内纯黑。禁止：不要出现洞内人物或光源。
```

## Clip 06 · 咯咯声

事实卡：

```text
原文范围：“轻点声……听！有动静！”至“蛤蟆叫一样的从洞里发出来。”
可见人物：老三
需要参考图：assets/images/scenes/scene_盗洞口_action_area.png；assets/images/characters/char_老三_identity.png；assets/images/props/prop_土耗子_identity.png
地点：盗洞口
关键道具：黑洞口、绳子
开始状态：老三听洞下人声。
结束状态：老三被未知咯咯声吓住，不敢出声。
不可错事实：咯咯声来自洞内黑暗，不显示来源。
```

戏剧卡：

```text
主要欲望：老三想听清下面发生什么。
阻力：洞口只传来怪声，没有画面信息。
状态变化：主动喊话 -> 被迫静止。
观众感受：看不见的东西开始接管场面。
行为链：听见警告；按住绳；洞口静止；第一声咯咯；肩膀一抖；慢慢后缩；洞口变成威胁来源。
```

提示词卡：

```text
事实：老三听见洞下老烟头说“轻点声……听！有动静！”，随后洞里传出蛤蟆一样的咯咯声。
上传顺序：@图片1=assets/images/scenes/scene_盗洞口_action_area.png；@图片2=assets/images/characters/char_老三_identity.png；@图片3=assets/images/props/prop_土耗子_identity.png
Seedance 直贴提示词：
使用 @图片1 锁定黑洞口，@图片2 锁定老三，@图片3 锁定绳子。生成 9:16 竖屏视频，约 6 秒，7 镜头。核心情绪：看不见的东西开始发声。
Shot 1，近景，0.8秒：老三听到洞底断续的“轻点声”，立刻闭嘴。
Shot 2，手部特写，0.7秒：他的手按住绳子，不敢再拉。
Shot 3，洞口极近，0.7秒：绳子和洞口边草叶都静止。
Shot 4，黑洞特写，0.8秒：洞里传出第一声咯咯。
Shot 5，老三近景，0.7秒：老三肩膀一抖，强迫自己低头听。
Shot 6，侧面中近景，0.8秒：第二声更近，他慢慢后缩。
Shot 7，关系全景，1.5秒：老三跪在洞边，黑洞像在盯着他。
灯光：月光只照洞口外沿。禁止：不要把声音来源画出来。
```

## Clip 07 · 绳子反拉

事实卡：

```text
原文范围：“三伢子，拉！”至“就算是匹骡子，他也能顶一顶。”
可见人物：老三
需要参考图：assets/images/scenes/scene_盗洞口_action_area.png；assets/images/characters/char_老三_identity.png；assets/images/props/prop_土耗子_identity.png
地点：盗洞口
关键道具：土耗子、绳尾、洞口
开始状态：老三听命拉绳。
结束状态：老三把绳尾绑腰，用全身重量和洞内反力僵持。
不可错事实：未知力量不露面，只通过绳子反拉表现。
```

戏剧卡：

```text
主要欲望：老三想把洞里的人和土耗子拉出来。
阻力：洞内反向力量把他拖向洞口。
状态变化：守绳少年 -> 拔河对抗者。
观众感受：怪物力量第一次有了物理重量。
行为链：洞内喊拉；猛拽；绳子反绷；脚滑近洞；绑腰；身体后倒；僵持。
```

提示词卡：

```text
事实：洞内老二大喊“三伢子，拉！”，老三猛拉土耗子，绳子被洞内反向拖拽，他把绳尾绑在腰上用全身重量僵持。
上传顺序：@图片1=assets/images/scenes/scene_盗洞口_action_area.png；@图片2=assets/images/characters/char_老三_identity.png；@图片3=assets/images/props/prop_土耗子_identity.png
Seedance 直贴提示词：
使用 @图片1 锁定盗洞口和绳子入洞位置，@图片2 锁定老三，@图片3 锁定土耗子。生成 9:16 竖屏视频，约 7 秒，8 个镜头。核心情绪：洞里的力量第一次通过绳子抓住老三。
Shot 1，中景，0.8秒：老三听见洞里大喊“三伢子，拉！”
Shot 2，动作近景，0.8秒：他双手猛拽绳尾，身体向后退。
Shot 3，绳子特写，0.7秒：绳子突然反向绷直，纤维拉紧。
Shot 4，低角度，0.8秒：老三脚掌刮过湿土，身体被拖向洞口。
Shot 5，手部特写，0.8秒：他急忙把绳尾绕到腰上勒紧。
Shot 6，侧面中景，0.9秒：老三身体后倒成斜线，双脚死撑地面。
Shot 7，洞口特写，0.8秒：绳子从洞口中央绷直进纯黑。
Shot 8，全景，1.4秒：老三和洞内未知力量僵持不动。
灯光：月光勾出绳子冷白边。禁止：不要显示洞内怪物。
```

## Clip 08 · 枪响弹出

事实卡：

```text
原文范围：“僵持了有十几秒”至“扭头就跑！”
可见人物：老三
需要参考图：assets/images/scenes/scene_盗洞口_action_area.png；assets/images/characters/char_老三_identity.png；assets/images/props/prop_土耗子_identity.png；assets/images/props/prop_匣子炮_identity.png
地点：盗洞口
关键道具：土耗子、匣子炮声音、弹出物
开始状态：老三和洞内力量僵持。
结束状态：土耗子弹出，老三接住后逃离洞口。
不可错事实：枪响来自洞内；大胡子喊“快跑”；洞内战斗不展示。
```

戏剧卡：

```text
主要欲望：老三想继续救人。
阻力：枪响和父亲喊跑说明救援已经失败。
状态变化：救援僵持 -> 带着未知结果逃跑。
观众感受：洞下把代价吐回地面。
行为链：绳子绷紧；枪响；喊跑；绳子卸力；土耗子弹出；本能接住；转身逃跑。
```

提示词卡：

```text
事实：僵持后洞内一声匣子炮响，大胡子喊老三快跑，绳子突然一松，土耗子弹出，老三接住后逃跑。
上传顺序：@图片1=assets/images/scenes/scene_盗洞口_action_area.png；@图片2=assets/images/characters/char_老三_identity.png；@图片3=assets/images/props/prop_土耗子_identity.png；@图片4=assets/images/props/prop_匣子炮_identity.png
Seedance 直贴提示词：
使用 @图片1 锁定洞口，@图片2 锁定老三，@图片3 锁定土耗子，@图片4 只作为洞内枪响和后续归属参考。生成 9:16 竖屏视频，约 6 秒，7 镜头。核心情绪：救援失败，洞里把结果吐出来。
Shot 1，侧面中景，0.8秒：老三腰间绳子绷紧，身体还在死撑。
Shot 2，老三近景，0.7秒：洞内一声枪响，他整个人僵住。
Shot 3，洞口特写，0.7秒：洞里传来大胡子嘶喊“快跑！”
Shot 4，绳子特写，0.8秒：绳子突然卸力，向外弹出。
Shot 5，动作近景，0.8秒：土耗子嗖地飞出，老三本能伸手接住。
Shot 6，老三近景，0.7秒：他怀里多出沉物，但不敢低头细看。
Shot 7，全景，1.5秒：老三抱着东西转身狂跑离开洞口。
灯光：枪响只用短暂反应表现，不照亮洞内。禁止：不要展示洞内战斗。
```

## Clip 09 · 断臂确认

事实卡：

```text
原文范围：“他一口气跑出有二里多地”至“想回去救他二哥和老爹”
可见人物：老三
需要参考图：assets/images/scenes/scene_荒野林地_action_area.png；assets/images/characters/char_老三_identity.png；assets/images/props/prop_土耗子_identity.png；assets/images/props/prop_老二断臂_fist.png
地点：荒野林地
关键道具：土耗子、老二断臂·握拳
开始状态：老三逃到林地喘息。
结束状态：老三认出老二断臂，决定回头救人。
不可错事实：断臂是老二的；老三先哭后咬牙。
```

戏剧卡：

```text
主要欲望：老三想确认怀里弹出来的东西。
阻力：结果物证明亲人已经遭遇重创。
状态变化：逃命者 -> 想回救亲人的见证者。
观众感受：恐怖落到亲情代价。
行为链：冲进林地；掏土耗子；断臂露出；认出；哭；咬牙；转身回救。
```

提示词卡：

```text
事实：老三跑到荒野林地停下，查看怀里的土耗子，发现上面勾着老二的断臂，哭后咬牙想回去救人。
上传顺序：@图片1=assets/images/scenes/scene_荒野林地_action_area.png；@图片2=assets/images/characters/char_老三_identity.png；@图片3=assets/images/props/prop_土耗子_identity.png；@图片4=assets/images/props/prop_老二断臂_fist.png
Seedance 直贴提示词：
使用 @图片1 锁定荒野林地，@图片2 锁定老三，@图片3 锁定土耗子，@图片4 锁定断臂。生成 9:16 竖屏视频，约 6 秒，7 镜头。核心情绪：未知恐怖变成亲人的代价。
Shot 1，中远景，0.8秒：老三冲进林地，扶着树停下喘气。
Shot 2，中近景，0.7秒：他低头掏出怀里的土耗子。
Shot 3，道具特写，0.8秒：断臂和握拳露出，挂在土耗子上。
Shot 4，老三近景，0.7秒：老三手一抖，认出那是老二的手。
Shot 5，极近表情，0.7秒：他哭出声，眼泪和恐惧混在一起。
Shot 6，近景，0.8秒：老三咬牙抱紧断臂，强迫自己站稳。
Shot 7，关系全景，1.5秒：他转身准备往土丘方向回去。
灯光：林地被树冠遮暗，断臂只给短促可读特写。禁止：不要让断臂变成完整尸体。
```

## Clip 10 · 回头见血尸

事实卡：

```text
原文范围：“刚一回头”至“正直勾勾地看着他。”
可见人物：老三、血尸
需要参考图：assets/images/scenes/scene_荒野林地_action_area.png；assets/images/characters/char_老三_identity.png；assets/images/characters/char_血尸_identity.png；assets/images/props/prop_匣子炮_identity.png
地点：荒野林地
关键道具：匣子炮
开始状态：老三准备回盗洞救人。
结束状态：血尸蹲在背后，切断回头路。
不可错事实：血尸先蹲伏凝视，不立刻扑击。
```

戏剧卡：

```text
主要欲望：老三想回去救老二和父亲。
阻力：血尸无声出现在身后。
状态变化：回救决心 -> 被迫对峙。
观众感受：回去和逃跑都不安全。
行为链：抱物转身；脚步停；树影血红；慢慢回头；血尸凝视；摸枪；对峙轴线成立。
```

提示词卡：

```text
事实：老三想回去救人，刚回头看见背后蹲着血红的东西，直勾勾看着他。
上传顺序：@图片1=assets/images/scenes/scene_荒野林地_action_area.png；@图片2=assets/images/characters/char_老三_identity.png；@图片3=assets/images/characters/char_血尸_identity.png；@图片4=assets/images/props/prop_匣子炮_identity.png
Seedance 直贴提示词：
使用 @图片1 锁定林地，@图片2 锁定老三，@图片3 锁定血尸，@图片4 锁定匣子炮。生成 9:16 竖屏视频，约 6 秒，7 镜头。核心情绪：回救的路被血尸堵住。
Shot 1，中景，0.8秒：老三抱着土耗子和断臂转身，准备往回跑。
Shot 2，脚步近景，0.7秒：他刚迈半步就停住。
Shot 3，主观中远景，0.8秒：右后方树影里蹲着血红轮廓。
Shot 4，老三近景，0.7秒：老三慢慢回头，眼神定住。
Shot 5，血尸近景，0.8秒：血尸蹲在暗部，直勾勾看着他，没有动。
Shot 6，手部近景，0.7秒：老三右手摸向腰间匣子炮。
Shot 7，对峙全景，1.5秒：老三在左前，血尸在右后暗部，回去的方向被切断。
灯光：树冠遮住大部分月光，只让血尸轮廓可读。禁止：不要让血尸提前扑击。
```

## Clip 11 · 贴脸开枪

事实卡：

```text
原文范围：“想到这里”至“向后退了好几步。”
可见人物：老三、血尸
需要参考图：assets/images/scenes/scene_荒野林地_action_area.png；assets/images/characters/char_老三_identity.png；assets/images/characters/char_血尸_identity.png；assets/images/props/prop_匣子炮_identity.png
地点：荒野林地
关键道具：匣子炮
开始状态：老三边退边拔枪。
结束状态：老三近距离连发，短暂打退血尸。
不可错事实：血尸贴脸扑来；老三后倒开枪；血尸不死，只后退。
```

戏剧卡：

```text
主要欲望：老三想用物理武器压住血尸。
阻力：血尸突然贴脸扑击。
状态变化：恐惧后退 -> 短暂反击成功。
观众感受：少年在极限距离里抢到主动。
行为链：后退拔枪；血尸站起；猛扑贴脸；后倒顶枪；连发；血尸后退；老三短暂庆幸。
```

提示词卡：

```text
事实：老三后退拔匣子炮，血尸站起扑到脸前，老三后倒近距离连发，把血尸打退几步。
上传顺序：@图片1=assets/images/scenes/scene_荒野林地_action_area.png；@图片2=assets/images/characters/char_老三_identity.png；@图片3=assets/images/characters/char_血尸_identity.png；@图片4=assets/images/props/prop_匣子炮_identity.png
Seedance 直贴提示词：
使用 @图片1 锁定林地对峙轴线，@图片2 锁定老三，@图片3 锁定血尸，@图片4 锁定匣子炮。生成 9:16 竖屏视频，约 6 秒，7 镜头。核心情绪：少年在贴脸恐惧里抢到一次主动。
Shot 1，中景，0.8秒：老三一边后退一边拔出匣子炮。
Shot 2，血尸中景，0.7秒：血尸从蹲伏慢慢站起，身体向前弓。
Shot 3，突进近景，0.7秒：血尸猛扑到老三鼻尖前。
Shot 4，动作近景，0.8秒：老三顺势后倒，枪口顶向血尸胸口。
Shot 5，枪口和胸口近景，0.8秒：匣子炮连发，火光短促闪动。
Shot 6，血尸反应，0.8秒：血尸被打得后退几步，身体晃动。
Shot 7，老三近景，1.4秒：老三喘着气，眼里出现短暂庆幸。
灯光：枪火只短闪，不改变整场冷月光。禁止：不要把血尸打死。
```

## Clip 12 · 卡壳翻盘

事实卡：

```text
原文范围：“再一回手对准那东西的脑袋”至“扭头就跑。”
可见人物：老三、血尸
需要参考图：assets/images/scenes/scene_荒野林地_action_area.png；assets/images/characters/char_老三_identity.png；assets/images/characters/char_血尸_identity.png；assets/images/props/prop_匣子炮_identity.png
地点：荒野林地
关键道具：匣子炮
开始状态：老三以为能补枪结束。
结束状态：枪卡壳，老三抡枪砸出后逃跑。
不可错事实：卡壳是转折；枪不再开火。
```

戏剧卡：

```text
主要欲望：老三想补枪彻底解决血尸。
阻力：旧匣子炮关键时刻失灵。
状态变化：短暂优势 -> 彻底逃亡。
观众感受：安全感被“喀嚓”空响掐断。
行为链：瞄头；扣扳机；空响；表情塌掉；血尸压近；抡枪；逃跑。
```

提示词卡：

```text
事实：老三想补枪打头，匣子炮喀嚓卡壳；他把枪抡出去，转身逃跑。
上传顺序：@图片1=assets/images/scenes/scene_荒野林地_action_area.png；@图片2=assets/images/characters/char_老三_identity.png；@图片3=assets/images/characters/char_血尸_identity.png；@图片4=assets/images/props/prop_匣子炮_identity.png
Seedance 直贴提示词：
使用 @图片1 锁定林地，@图片2 锁定老三，@图片3 锁定血尸，@图片4 锁定匣子炮。生成 9:16 竖屏视频，约 6 秒，7 镜头。核心情绪：安全感被一声卡壳掐断。
Shot 1，中近景，0.8秒：老三回手把枪口对准血尸头部。
Shot 2，扳机特写，0.7秒：手指扣下，只有喀嚓空响。
Shot 3，老三极近，0.7秒：老三脸上的庆幸瞬间塌掉。
Shot 4，血尸中景，0.8秒：血尸继续从右前方压近。
Shot 5，动作近景，0.8秒：老三抡圆胳膊把匣子炮砸出去。
Shot 6，中景，0.7秒：他不看有没有砸中，转身冲向大树。
Shot 7，全景，1.5秒：老三逃入树影，血尸在后方重新逼近。
灯光：冷月光，枪械卡壳用动作和表情表达。禁止：不要让枪继续开火。
```

## Clip 13 · 趴地装死

事实卡：

```text
原文范围：“看准前面一颗大树”至“血尸从他身上踩了过去”
可见人物：老三、血尸
需要参考图：assets/images/scenes/scene_荒野林地_action_area.png；assets/images/characters/char_老三_identity.png；assets/images/characters/char_血尸_identity.png；assets/images/characters/char_老三_tired.png
地点：荒野林地树墩旁
关键道具：树墩作为场景机制
开始状态：老三拼命逃跑。
结束状态：老三趴地被血尸踩过，进入中毒末态。
不可错事实：老三被树墩绊倒；血尸踩过而不是抓起他。
```

戏剧卡：

```text
主要欲望：老三想跑到树边躲开。
阻力：树墩绊倒、血尸追到背后。
状态变化：奔逃 -> 装死 -> 中毒。
观众感受：唯一能做的动作是不动。
行为链：冲向大树；脚绊；扑倒；拍地停住；趴平；血尸踩过；背部中毒印记。
```

提示词卡：

```text
事实：老三逃跑时被树墩绊倒，脸磕地；听见身后风声后趴地不动，血尸从他背上踩过，留下中毒印记。
上传顺序：@图片1=assets/images/scenes/scene_荒野林地_action_area.png；@图片2=assets/images/characters/char_老三_identity.png；@图片3=assets/images/characters/char_血尸_identity.png；@图片4=assets/images/characters/char_老三_tired.png
Seedance 直贴提示词：
使用 @图片1 锁定树墩和贴地林地，@图片2 锁定老三正常状态，@图片3 锁定血尸，@图片4 锁定踩后虚弱状态。生成 9:16 竖屏视频，约 6 秒，7 镜头。核心情绪：逃跑失败后，他靠不动活下来。
Shot 1，追跑中景，0.8秒：老三冲向一棵大树。
Shot 2，脚部特写，0.7秒：脚被半掩树墩绊住。
Shot 3，低角度，0.8秒：老三整个人扑倒，脸磕在地面边缘。
Shot 4，手掌特写，0.7秒：他狠狠拍地，又听见身后风声。
Shot 5，贴地近景，0.8秒：老三索性趴平不动，屏住呼吸。
Shot 6，上压动作，0.8秒：血尸脚掌从上方踩过他的背后继续离开。
Shot 7，老三低位近景，1.4秒：老三背部出现深褐湿印，眼神开始发虚。
灯光：人物低位多在暗部，血尸只给上压局部。禁止：不要让血尸抓起老三。
```

## Clip 14 · 取帛片

事实卡：

```text
原文范围：“背上那被踩过地方”至“塞进了自己袖子里。”
可见人物：老三
需要参考图：assets/images/scenes/scene_荒野林地_action_area.png；assets/images/characters/char_老三_tired.png；assets/images/props/prop_老二断臂_cloth.png；assets/images/props/prop_古帛片_identity.png
地点：荒野林地贴地低位
关键道具：老二断臂·握帛片、古帛片
开始状态：老三中毒趴地，视线发糊。
结束状态：古帛片从断臂转移到老三袖中。
不可错事实：老三爬过去掰开手指，不是站立拿取。
```

戏剧卡：

```text
主要欲望：老三想保存二哥拼命带出的东西。
阻力：毒性猛烈，身体几乎不能动。
状态变化：濒死无力 -> 完成线索转移。
观众感受：恐怖落到“不能白断、不能白死”的执念。
行为链：趴地发作；看见帛片；拖身爬行；碰到断臂；掰手指；取出帛片；塞进袖中。
```

提示词卡：

```text
事实：老三中毒趴地，看到老二断臂手里握着古帛片；他爬过去掰开手指，把帛片塞进自己袖子。
上传顺序：@图片1=assets/images/scenes/scene_荒野林地_action_area.png；@图片2=assets/images/characters/char_老三_tired.png；@图片3=assets/images/props/prop_老二断臂_cloth.png；@图片4=assets/images/props/prop_古帛片_identity.png
Seedance 直贴提示词：
使用 @图片1 锁定贴地林地，@图片2 锁定老三中毒趴卧状态，@图片3 锁定断臂握帛片，@图片4 锁定古帛片。生成 9:16 竖屏视频，约 7 秒，8 镜头。核心情绪：濒死前把二哥拼命带出的东西保存下来。
Shot 1，贴地近景，0.8秒：老三趴着，背部印记发作，眼前发糊。
Shot 2，主观模糊，0.8秒：不远处断臂手心露出古帛片一角。
Shot 3，低位中景，0.8秒：老三用手肘拖着身体往前爬。
Shot 4，手部近景，0.8秒：他的手碰到老二断臂，指尖发抖。
Shot 5，极近特写，0.8秒：老三用力掰开僵硬手指。
Shot 6，道具特写，0.8秒：古帛片从掌心露出来。
Shot 7，动作近景，0.8秒：老三把帛片塞进自己袖子。
Shot 8，关系落点，1.4秒：断臂留在地上，线索已经转到老三身上。
灯光：贴地冷月光，视线可轻微虚焦。禁止：不要让老三站起来。
```

## Clip 15 · 无瞳怪脸

事实卡：

```text
原文范围：“这个时候他的耳朵也开始蜂鸣了”至结尾。
可见人物：老三、第二实体局部怪脸
需要参考图：assets/images/scenes/scene_荒野林地_action_area.png；assets/images/characters/char_老三_tired.png；assets/images/characters/char_第二实体怪脸_partial.png
地点：荒野林地贴地低位
关键道具：古帛片已在袖中，不需要再展示
开始状态：老三中毒意识模糊，听见熟悉咯咯声。
结束状态：无瞳怪脸从上方压进画面看着他。
不可错事实：第二实体只局部揭示，不完整亮相；眼睛没有瞳孔；老三趴在地上。
```

戏剧卡：

```text
主要欲望：老三想在昏迷前理解咯咯声来源。
阻力：尸毒让他无法思考，威胁已经压到头顶。
状态变化：以为血尸是主威胁 -> 发现还有另一张无瞳怪脸。
观众感受：最后一秒推翻认知。
行为链：耳鸣；听见咯咯；意识到血尸没叫；艰难抬头；怪脸上压；无瞳眼下看；老三被观察。
```

提示词卡：

```text
建议模型：Seedance 2.0
建议模式：image-to-video，多图参考
画幅：9:16
时长：6 秒
镜头数：7

上传顺序：
@图片1 = assets/images/scenes/scene_荒野林地_action_area.png
@图片2 = assets/images/characters/char_老三_tired.png
@图片3 = assets/images/characters/char_第二实体怪脸_partial.png

直贴提示词：
使用 @图片1 锁定荒野林地低位，@图片2 锁定老三中毒趴地状态，@图片3 锁定第二实体的局部怪脸。生成 9:16 竖屏视频，约 6 秒，7 个镜头。核心情绪：真正的未知从上方压到眼前。
Shot 1，贴地近景，0.8秒：老三趴在草地里发冷，眼神涣散。
Shot 2，耳侧极近，0.7秒：他耳边蜂鸣，远处传来咯咯声。
Shot 3，老三眼睛特写，0.7秒：他迟钝地意识到刚才血尸没有叫过。
Shot 4，低角度近景，0.8秒：老三艰难抬起头。
Shot 5，主观上方，0.8秒：画面上方有巨大怪脸局部慢慢压下来。
Shot 6，眼部极近，0.8秒：两只无瞳空眼直直向下看。
Shot 7，关系落点，1.4秒：老三趴在画面下方，怪脸压在上方，画面停在被观察的关系上。
灯光：林地大面积暗部，怪脸边缘只有冷白月光勾出。
表演：老三几乎无力，只剩条件反射抬头。
禁止：不要展示第二实体全身；不要让怪脸张牙舞爪攻击；不要出现额外怪物。
```
