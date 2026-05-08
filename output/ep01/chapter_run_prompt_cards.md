# Chapter Run Prompt Cards · 血尸章节

This run follows the first-principles workflow:

```text
Facts -> Drama -> Shot Chain -> Prompt -> Review
```

Chapter strategy:

- Do not adapt every sentence.
- Convert the chapter into short playable video clips.
- Each clip has one behavior change or information turn.
- Character drama uses 6s / 7 shots by default.
- Threat / mechanism beats use 5-8s with 4-7 shots.

Global style for all cards:

```text
9:16 vertical Chinese suspense manga style, rough ink lines, realistic eastern characters, 1960s-1970s rural Hunan tomb-raider era, no modern objects. Cold blue-white moonlight cuts from upper right; right faces and shoulders have rim light, left sides fall into shadow. Cave interiors and forest depths stay pure black unless a reveal shot says otherwise.
```

## Chapter Drama Spine

```text
01 血土钩子:
normal excavation detail -> impossible wet omen

02 老烟头定性:
silent confusion -> named danger

03 老二顶撞:
gun-backed swagger -> embarrassed restraint

04 老三被呵斥:
young protest -> physically shut down -> forced into rope-guard role

05 洞口等待:
bored waiting -> hears wrongness below

06 拉绳反力:
rescue pull -> invisible tug-of-war

07 枪响逃跑:
standoff -> gunshot -> rope release -> survival flight

08 断手与血红东西:
escaped relief -> personal loss -> decision to return -> ambushed by presence

09 血尸站起:
terror -> practical fighting stance

10 近身扑杀:
instinctive defense -> temporary success -> weapon failure

11 装死被踩:
flight -> fall -> chooses stillness -> survives but is poisoned

12 帛片与第二怪脸:
dying confusion -> preserves clue -> realizes the first monster was not the final threat
```

---

## Clip 01 · 血土钩子

Fact Card:

```text
Excerpt: lines 2-4
Visible characters: none
Required references: Luoyang shovel head, wilderness mound
Location: Biaoziling wilderness mound at night
Key props: Luoyang shovel head with abnormal deep reddish-brown wet soil
Start state: four men are offscreen; the ground is silent
End state: the abnormal soil becomes the first omen
Non-negotiables: no people in this clip; abnormal liquid is the only warm color
```

Drama Card:

```text
Main desire: the image wants to hook the viewer before anyone explains it
Opposition: the object is silent and ordinary-looking until the wet color appears
State change: normal excavation tool -> impossible omen
Viewer feeling: something under the soil is already wrong
Behavior chain:
1. Empty moonlit soil holds still.
2. The shovel head is found in extreme close-up.
3. Damp soil darkens around the metal edge.
4. A deep reddish-brown wetness slowly spreads.
5. Moonlight catches the metal and the wet soil differently.
6. The frame holds long enough for the viewer to understand the omen.
```

Prompt Card:

```text
Recommended model: Seedance 2.0
Recommended mode: image-to-video
Aspect ratio: 9:16
Duration: about 5 seconds
Shot count: 5

Upload order:
@Image1 = assets/images/prop_洛阳铲铲头_main.png
@Image2 = assets/images/scene_镖子岭土丘_main.png

Direct prompt:
Use @Image1 to lock the Luoyang shovel head and @Image2 to lock the moonlit wilderness mound. Generate a 9:16 vertical Chinese suspense manga video, about 5 seconds, 5 quiet shots. Core emotion: an ordinary excavation detail becomes the first impossible omen.

Shot 1, empty ground close-up, 0.8s: Moonlit yellow-brown soil and low grass sit completely still, no people visible.
Shot 2, extreme insert, 1.0s: The Luoyang shovel head is half-buried in the soil; cold moonlight creates a thin edge highlight on the metal.
Shot 3, macro detail, 1.0s: Damp soil at the shovel mouth slowly darkens, as if moisture is spreading from underground.
Shot 4, extreme close-up, 1.2s: A deep reddish-brown wetness gathers around the shovel edge, the only warm color in the cold blue night.
Shot 5, held omen shot, 1.0s: The frame holds on the shovel head and wet soil; nothing explains it, the silence makes it worse.

Lighting: Cold blue-white moonlight from upper right; soil and grass stay dark and cold, the wet reddish-brown detail is the only warm accent.
Do not show any people, dialogue, modern objects, cave interior, or extra tools.
```

---

## Clip 02 · 老烟头定性

Fact Card:

```text
Excerpt: line 5
Visible characters: Old Yantou, Big Beard, Old Er, Old San
Required references: all four characters, Luoyang shovel head, smoking pipe, mound
Location: mound top at night
Key props: Luoyang shovel head, smoking pipe
Start state: four men stare at the abnormal shovel
End state: Old Yantou names it as a blood corpse below
Non-negotiables: Old Yantou controls the mood; reactions are staggered
```

Drama Card:

```text
Main desire: the group wants an explanation
Opposition: the explanation is worse than ignorance
State change: confused silence -> named danger
Viewer feeling: the old man knows something the young men do not
Behavior chain:
1. Four men stare at the shovel.
2. Old Yantou taps the smoking pipe on the ground.
3. Big Beard and Old Er wait for his judgment.
4. Old Yantou quietly says the thing below is a blood corpse.
5. Old Er's bravado pauses for half a beat.
6. Big Beard's jaw tightens.
7. Old San looks from the shovel to the black night, suddenly smaller.
```

Prompt Card:

```text
Recommended model: Seedance 2.0
Recommended mode: image-to-video, multi-shot
Aspect ratio: 9:16
Duration: about 6 seconds
Shot count: 7

Upload order:
@Image1 = assets/images/char_老烟头_main.png
@Image2 = assets/images/char_大胡子_main.png
@Image3 = assets/images/char_老二·独眼二伢子_main.png
@Image4 = assets/images/char_老三_main.png
@Image5 = assets/images/scene_镖子岭土丘_main.png
@Image6 = assets/images/prop_洛阳铲铲头_main.png
@Image7 = assets/images/prop_旱烟枪_main.png

Direct prompt:
Use @Image1 to lock Old Yantou, @Image2 Big Beard, @Image3 one-eyed Old Er, @Image4 Old San, @Image5 the mound, @Image6 the Luoyang shovel head, and @Image7 the smoking pipe. Generate a 9:16 vertical Chinese suspense manga video, about 6 seconds, 7 shots. Core emotion: the old man quietly names the danger and the whole group changes temperature.

Shot 1, side medium-wide, 0.8s: Four men crouch or stand around the abnormal shovel head on the mound. Nobody speaks. The shovel is the center.
Shot 2, smoking pipe insert, 0.6s: Old Yantou taps the smoking pipe against the ground, small and deliberate.
Shot 3, Old Yantou close-up, 0.9s: He looks at the shovel first, then raises his eyes slightly, calm and heavy.
Shot 4, two-shot reaction, 0.8s: Big Beard and Old Er wait; Old Er still carries a trace of arrogance, Big Beard is tense.
Shot 5, Old Yantou medium close-up, 0.9s: He quietly says the thing below is a blood corpse, not shouting, just settling the air.
Shot 6, staggered reaction close-ups, 1.2s: Old Er's mouth stops mid-breath; Big Beard's jaw tightens; Old San's eyes widen a little.
Shot 7, group landing, 0.8s: The group is still around the shovel, but now the black ground below them feels like the real subject.

Lighting: Cold moonlight from upper right; faces half-lit, left sides dark. The shovel wetness remains the only warm accent.
Do not make everyone look at the camera. Do not turn the scene into a speech. Keep reactions staggered and quiet.
```

---

## Clip 03 · 老二顶撞

Fact Card:

```text
Excerpt: lines 6-12
Visible characters: Old Er, Old Yantou, Big Beard, Old San
Required references: all four characters, smoking pipe, pistol, shovel/mound
Location: mound top
Key props: smoking pipe, Mauser pistol detail
Start state: Old Yantou has named the danger
End state: Old Er's bravado is mocked and knocked down
Non-negotiables: Old Er is one-eyed; Big Beard is his father; Old Yantou blocks violence with pipe
```

Drama Card:

```text
Main desire: Old Er wants to prove he can handle the danger with a gun
Opposition: Old Yantou and Big Beard treat him as reckless
State change: swagger -> embarrassed restraint
Viewer feeling: youth and guns are not enough for what is below
Behavior chain:
1. Old Er steps into the pressure line and talks big.
2. His hand brushes the pistol at his waist.
3. Big Beard snaps at him.
4. Old Er tries to answer back.
5. Big Beard raises a hand to hit him.
6. Old Yantou's smoking pipe blocks the strike.
7. Old Er lowers his head and smirks, then gets tapped down by Old Yantou.
```

Prompt Card:

```text
Recommended model: Seedance 2.0
Recommended mode: image-to-video, multi-shot
Aspect ratio: 9:16
Duration: about 6 seconds
Shot count: 7

Upload order:
@Image1 = assets/images/char_老二·独眼二伢子_main.png
@Image2 = assets/images/char_老烟头_main.png
@Image3 = assets/images/char_大胡子_main.png
@Image4 = assets/images/char_老三_main.png
@Image5 = assets/images/scene_镖子岭土丘_main.png
@Image6 = assets/images/prop_旱烟枪_main.png
@Image7 = assets/images/prop_匣子炮_main.png

Direct prompt:
Use @Image1 to lock one-eyed Old Er, @Image2 Old Yantou, @Image3 Big Beard, @Image4 Old San, @Image5 the mound, @Image6 the smoking pipe, and @Image7 the old Mauser pistol. Generate a 9:16 vertical Chinese suspense manga video, about 6 seconds, 7 fast shots. Core emotion: Old Er tries to turn fear into swagger, but the older men shut him down.

Shot 1, side medium-wide, 0.8s: Old Er steps forward from the group, body angled toward Old Yantou, the others around the mound.
Shot 2, waist insert, 0.6s: Old Er's hand brushes the old Mauser pistol at his waist, showing where his confidence comes from.
Shot 3, Old Er close-up, 0.8s: He speaks with a hard mouth and raised chin, one eye glaring, reckless and proud.
Shot 4, Big Beard medium close-up, 0.8s: Big Beard snaps at him, brow lowered, shoulders pushing forward like he wants to hit him.
Shot 5, action close-up, 0.7s: Big Beard's hand rises, but Old Yantou's smoking pipe cuts across and stops it.
Shot 6, Old Yantou close-up, 1.0s: Old Yantou smiles without warmth, scolds the father and son together, completely unhurried.
Shot 7, reaction landing, 1.3s: Old Er lowers his head with a brief embarrassed smirk; Old Yantou taps him with the pipe, and Old San watches from the edge.

Lighting: Cold moonlight from upper right, strong shadows, rough manga ink lines.
Do not confuse Old Er with Big Beard. Do not make the gun modern. Do not stage it as everyone facing the camera.
```

---

## Clip 04 · 老三被呵斥

Prompt Card:

```text
Recommended model: Seedance 2.0
Recommended mode: image-to-video, multi-shot
Aspect ratio: 9:16
Duration: about 6 seconds
Shot count: 7

Upload order:
@Image1 = assets/images/char_老三_main.png
@Image2 = assets/images/char_老二·独眼二伢子_main.png
@Image3 = assets/images/char_老烟头_main.png
@Image4 = assets/images/char_大胡子_main.png
@Image5 = assets/images/scene_盗洞口_main.png
@Image6 = assets/images/prop_土耗子_main.png
@Image7 = assets/images/prop_旱烟枪_main.png

Direct prompt:
Use @Image1 to lock Old San, @Image2 one-eyed Old Er, @Image3 Old Yantou, @Image4 Big Beard, @Image5 the night cave mouth, @Image6 the rope tool, and @Image7 the smoking pipe. Generate a 9:16 vertical Chinese suspense manga video, about 6 seconds, 7 fast shots. Core emotion: Old San is angry that he is not allowed to go down the cave; he talks back, gets physically shut down by his older brother, then has to swallow the protest while the others prepare to descend.

Shot 1, side medium-wide, 0.8s: The black cave mouth sits at lower right. Old Yantou stands near the cave mouth giving orders; Big Beard and Old Er are close to the descent line; Old San stands outside the group holding the tail end of the rope tool.
Shot 2, Old San close-up, 0.7s: Old San frowns and steps forward half a step, mouth opening to protest, eyes stubborn.
Shot 3, Old Yantou medium close-up, 0.7s: Old Yantou lightly blocks Old San with the smoking pipe, not really hitting him, half teasing and half commanding.
Shot 4, Old San extreme expression close-up, 0.6s: Old San still refuses to give in. His mouth twists and eyes glance aside, young and stubborn.
Shot 5, Old Er action close-up, 0.8s: One-eyed Old Er suddenly pushes in from the side and grabs Old San by the ear. The action is fast but readable.
Shot 6, Old San reaction close-up, 0.9s: Old San's head tilts from the ear being pulled; his stubbornness disappears. He looks toward Big Beard for help, but Big Beard is already turning away to gather gear.
Shot 7, group relationship landing, 1.5s: Old Er releases Old San. Old San rubs his ear with one hand and still holds the rope tool tail with the other. The three descent characters turn toward the black cave mouth while Old San remains outside the group.

Lighting: Cold moonlight from upper right; the cave mouth stays pure black.
Do not let anyone enter the cave in this clip. Do not turn the cave into stairs or a tunnel. Do not make Old San cry dramatically. Do not confuse Old Er with Big Beard.
```

---

## Clip 05 · 洞口等待，怪声出现

Prompt Card:

```text
Recommended model: Seedance 2.0
Recommended mode: image-to-video, multi-shot
Aspect ratio: 9:16
Duration: about 7 seconds
Shot count: 7

Upload order:
@Image1 = assets/images/char_老三_main.png
@Image2 = assets/images/scene_盗洞口_main.png
@Image3 = assets/images/prop_土耗子_main.png

Direct prompt:
Use @Image1 to lock Old San, @Image2 the night cave mouth, and @Image3 the rope tool. Generate a 9:16 vertical Chinese suspense manga video, about 7 seconds, 7 shots. Core emotion: Old San waits above the cave, bored and annoyed, then realizes something below has gone wrong.

Shot 1, wide cave-mouth shot, 0.8s: Old San sits or crouches alone beside the black cave mouth, holding the rope tool tail. The other men are unseen below.
Shot 2, Old San medium close-up, 0.9s: He grows impatient, leans toward the cave, and calls down.
Shot 3, cave-mouth insert, 0.8s: The black opening answers only with a delayed, muffled voice from below.
Shot 4, Old San close-up, 0.8s: His annoyance fades; he tilts his head, trying to hear.
Shot 5, rope-hand insert, 0.8s: His fingers tighten on the rope tail as a faint strange clicking-croaking sound comes from the dark.
Shot 6, reaction close-up, 1.2s: Old San stops breathing for a beat, eyes widening, mouth closing before he can speak again.
Shot 7, relationship landing, 1.7s: He remains above, small beside the cave mouth, listening into pure blackness while the rope in his hands becomes the only connection to the men below.

Lighting: Cold moonlight, cave mouth pure black, rope edge faintly rim-lit.
Do not show anyone inside the cave. Do not make the sound source visible. Do not add monsters yet.
```

---

## Clip 06 · 拉绳反力

Prompt Card:

```text
Recommended model: Seedance 2.0
Recommended mode: image-to-video, multi-shot
Aspect ratio: 9:16
Duration: about 7 seconds
Shot count: 7

Upload order:
@Image1 = assets/images/char_老三_main.png
@Image2 = assets/images/scene_盗洞口_main.png
@Image3 = assets/images/prop_土耗子_main.png

Direct prompt:
Use @Image1 to lock Old San, @Image2 the cave mouth, and @Image3 the rope tool. Generate a 9:16 vertical Chinese suspense manga video, about 7 seconds, 7 shots. Core emotion: a simple rescue pull becomes a tug-of-war with something hidden below.

Shot 1, medium-wide, 0.8s: Old San hears a shout from below and snaps into action beside the black cave mouth.
Shot 2, foot-and-rope insert, 0.7s: He plants one foot hard in the dirt and grabs the rope tail with both hands.
Shot 3, action medium shot, 0.9s: He pulls backward with his whole body; the rope slides out a little.
Shot 4, rope insert, 0.7s: The rope suddenly jerks the opposite direction, snapping taut toward the black hole.
Shot 5, Old San body shot, 1.0s: He almost gets dragged forward, knees bending and shoulders lurching toward the cave.
Shot 6, mechanism close-up, 1.2s: He quickly wraps or braces the rope against his waist, then leans backward with his full body weight.
Shot 7, standoff landing, 1.7s: Old San is leaned back at a hard angle, heels digging into dirt, rope taut into the pure black cave. The unseen force below holds him in place.

Lighting: Moonlight from upper right; rope has a thin cold rim light; cave interior stays pure black.
Do not show the thing below. Do not let Old San fall into the cave. Keep the body mechanics readable.
```

---

## Clip 07 · 枪响，绳松，逃跑

Prompt Card:

```text
Recommended model: Seedance 2.0
Recommended mode: image-to-video, multi-shot
Aspect ratio: 9:16
Duration: about 6 seconds
Shot count: 6

Upload order:
@Image1 = assets/images/char_老三_main.png
@Image2 = assets/images/scene_盗洞口_main.png
@Image3 = assets/images/prop_土耗子_main.png
@Image4 = assets/images/prop_匣子炮_main.png

Direct prompt:
Use @Image1 to lock Old San, @Image2 the cave mouth, @Image3 the rope tool bundle, and @Image4 the old Mauser pistol as a small prop detail. Generate a 9:16 vertical Chinese suspense manga video, about 6 seconds, 6 shots. Core emotion: the fight below breaks, the rope releases, and Old San chooses survival.

Shot 1, standoff medium shot, 0.8s: Old San leans back against the taut rope, fighting the unseen force below.
Shot 2, black cave insert, 0.6s: A sudden gunshot flashes faintly from inside the pure black cave, then darkness returns.
Shot 3, Old San close-up, 0.8s: He hears his father shout for him to run; fear hits his face instantly.
Shot 4, rope action insert, 0.8s: The rope suddenly goes slack and the rope tool bundle snaps upward out of the cave mouth.
Shot 5, catch close-up, 1.0s: Old San catches the bundle against his chest, barely understanding what is attached.
Shot 6, running medium shot, 2.0s: He turns and runs away from the cave without looking back, clutching the bundle.

Lighting: Cold moonlight outside; the gun flash is a very brief warm flicker only inside the cave.
Do not reveal people inside the cave. Do not clearly reveal the attached clue yet. Do not make the gun modern.
```

---

## Clip 08 · 认出断手，回头见血红东西

Prompt Card:

```text
Recommended model: Seedance 2.0
Recommended mode: image-to-video, multi-shot
Aspect ratio: 9:16
Duration: about 8 seconds
Shot count: 7

Upload order:
@Image1 = assets/images/char_老三_main.png
@Image2 = assets/images/scene_荒野林地_main.png
@Image3 = assets/images/prop_土耗子_main.png
@Image4 = assets/images/prop_老二断臂_fist.png
@Image5 = assets/images/char_血尸_main.png

Direct prompt:
Use @Image1 to lock Old San, @Image2 the dark wilderness forest, @Image3 the rope tool bundle, @Image4 the severed-arm clue in a non-graphic dark-brown manga treatment, and @Image5 the blood-corpse creature. Generate a 9:16 vertical Chinese suspense manga video, about 8 seconds, 7 shots. Core emotion: Old San escapes, identifies the terrible clue, decides to turn back, then discovers he is not alone.

Shot 1, forest medium-wide, 0.8s: Old San stops in the dark forest, bent over and breathing hard, still clutching the bundle.
Shot 2, object insert, 1.0s: He opens the bundle and sees a small dark-brown severed-arm clue attached to it, not huge, not graphic, but unmistakably personal.
Shot 3, Old San reaction close-up, 1.0s: He recognizes it as Old Er's. His face breaks for one second, then he clamps the emotion down.
Shot 4, decision close-up, 0.9s: He grits his teeth and turns his body as if he wants to go back to save them.
Shot 5, turning medium shot, 1.0s: His head turns first, then shoulders follow; the forest behind him enters the frame.
Shot 6, delayed reveal, 1.3s: In the dark behind him, a blood-red human-shaped thing crouches between tree trunks, watching him.
Shot 7, relationship landing, 2.0s: Old San freezes in the foreground with the bundle in his arms; the blood-red thing remains low and still in the background, both locked in the same axis.

Lighting: Forest is mostly black-green shadow with thin moon patches. The creature is only partially readable at first.
Do not make the severed clue oversized or graphic. Do not reveal the creature before Shot 6. Do not make it a zombie crowd; only one thing.
```

---

## Clip 09 · 血尸站起，老三拔枪

Prompt Card:

```text
Recommended model: Seedance 2.0
Recommended mode: image-to-video, multi-shot
Aspect ratio: 9:16
Duration: about 7 seconds
Shot count: 7

Upload order:
@Image1 = assets/images/char_老三_main.png
@Image2 = assets/images/char_血尸_main.png
@Image3 = assets/images/scene_荒野林地_main.png
@Image4 = assets/images/prop_匣子炮_main.png

Direct prompt:
Use @Image1 to lock Old San, @Image2 the blood-corpse creature, @Image3 the dark forest, and @Image4 the old Mauser pistol. Generate a 9:16 vertical Chinese suspense manga video, about 7 seconds, 7 shots. Core emotion: Old San is terrified, but he forces himself into a practical fighting stance.

Shot 1, two-plane medium-wide, 0.8s: Old San stands foreground left; the blood-corpse creature crouches in background shadow between trees.
Shot 2, creature medium shot, 0.8s: The creature slowly rises from its crouch, wet dark red-brown body catching tiny cold highlights.
Shot 3, Old San close-up, 0.8s: His face tightens with disgust and fear; eyes widen, mouth closes hard.
Shot 4, hand insert, 0.7s: His hand reaches to his waist and grips the old Mauser pistol.
Shot 5, medium action shot, 0.9s: He backs away while drawing the pistol, forcing the barrel toward the creature.
Shot 6, pistol close-up, 0.8s: The old pistol trembles slightly in his hands but stays aimed.
Shot 7, standoff landing, 2.2s: Old San retreats step by step, pistol raised; the creature stands fully now, silent and unnatural in the forest dark.

Lighting: Cold moon patches and black forest depth; creature highlights are minimal, not fully lit.
Do not make the pistol modern. Do not make Old San heroic and calm; he is scared but functional.
```

---

## Clip 10 · 近身扑杀，枪卡壳

Prompt Card:

```text
Recommended model: Seedance 2.0
Recommended mode: image-to-video, multi-shot
Aspect ratio: 9:16
Duration: about 8 seconds
Shot count: 8

Upload order:
@Image1 = assets/images/char_老三_main.png
@Image2 = assets/images/char_血尸_main.png
@Image3 = assets/images/scene_荒野林地_main.png
@Image4 = assets/images/prop_匣子炮_main.png

Direct prompt:
Use @Image1 to lock Old San, @Image2 the blood-corpse creature, @Image3 the forest, and @Image4 the old Mauser pistol. Generate a 9:16 vertical Chinese suspense manga action video, about 8 seconds, 8 fast shots. Core emotion: Old San survives the first attack by instinct, then his only weapon fails.

Shot 1, creature lunge medium shot, 0.7s: The creature suddenly folds forward and launches toward Old San.
Shot 2, Old San reaction close-up, 0.6s: Old San's eyes snap wide as the creature enters his space.
Shot 3, extreme proximity shot, 0.8s: The creature's face rushes close to Old San's face, too close and wrong.
Shot 4, falling-back action shot, 0.9s: Old San falls backward while firing the old Mauser upward at close range.
Shot 5, impact medium shot, 0.8s: Brief muzzle flashes push the creature back several steps; keep the impact stylized manga, not graphic.
Shot 6, Old San close-up, 0.8s: Old San thinks he has a chance, breath sharp, eyes locked.
Shot 7, pistol insert, 0.8s: He pulls the trigger again. The pistol jams with a hard mechanical click.
Shot 8, terror landing, 2.6s: Old San stares at the jammed pistol, then at the creature; the weapon is useless and the forest suddenly feels huge.

Lighting: Cold forest darkness with very brief warm muzzle flashes that vanish immediately.
Do not make the gun modern. Do not overplay gore. Keep the action readable and short.
```

---

## Clip 11 · 摔倒装死，被踩过去

Prompt Card:

```text
Recommended model: Seedance 2.0
Recommended mode: image-to-video, multi-shot
Aspect ratio: 9:16
Duration: about 8 seconds
Shot count: 8

Upload order:
@Image1 = assets/images/char_老三_main.png
@Image2 = assets/images/char_血尸_main.png
@Image3 = assets/images/scene_荒野林地_main.png
@Image4 = assets/images/prop_土耗子_main.png
@Image5 = assets/images/prop_老二断臂_fist.png

Direct prompt:
Use @Image1 to lock Old San, @Image2 the blood-corpse creature, @Image3 the forest, @Image4 the rope tool bundle, and @Image5 the dark-brown clue attached to it. Generate a 9:16 vertical Chinese suspense manga video, about 8 seconds, 8 shots. Core emotion: Old San's last trick is to stop acting alive.

Shot 1, running medium shot, 0.7s: Old San runs through the forest, clutching the bundle, not looking back.
Shot 2, foot insert, 0.6s: His foot catches on a hidden tree stump or root.
Shot 3, fall action shot, 0.9s: He crashes forward and hits the ground hard; the bundle slides slightly ahead of him.
Shot 4, ground close-up, 0.8s: Old San slaps the dirt in frustration, then hears the creature closing behind him.
Shot 5, decision close-up, 0.8s: His face hardens; instead of getting up, he forces himself flat against the ground.
Shot 6, low ground angle, 1.0s: The creature approaches from above the frame, heavy and unnatural.
Shot 7, pressure shot, 1.2s: The creature steps over him and presses one foot onto his back, then keeps moving. Old San clenches but does not cry out.
Shot 8, aftermath close-up, 2.0s: Old San remains flat and shaking, eyes unfocused, realizing something is wrong with his body.

Lighting: Forest mostly black, cold rim light along Old San's shoulder and the creature's edge.
Do not make the creature stop to attack again. Do not make Old San jump up. Keep the step stylized and non-graphic.
```

---

## Clip 12 · 帛片入袖，第二张怪脸

Prompt Card:

```text
Recommended model: Seedance 2.0
Recommended mode: image-to-video, multi-shot
Aspect ratio: 9:16
Duration: about 10 seconds
Shot count: 8

Upload order:
@Image1 = assets/images/char_老三_tired.png
@Image2 = assets/images/scene_荒野林地_main.png
@Image3 = assets/images/prop_老二断臂_cloth.png
@Image4 = assets/images/prop_古帛片_main.png
@Image5 = assets/images/char_第二实体怪脸_partial.png

Direct prompt:
Use @Image1 to lock poisoned exhausted Old San, @Image2 the dark forest, @Image3 the dark-brown hand clue holding the cloth fragment, @Image4 the ancient silk fragment, and @Image5 the partial huge eyeless face. Generate a 9:16 vertical Chinese suspense manga video, about 10 seconds, 8 shots. Core emotion: while dying, Old San chooses to preserve the clue, then realizes the first monster was not the final threat.

Shot 1, low exhausted medium shot, 1.0s: Old San lies weakly on the forest floor, vision blurred, one arm dragging forward.
Shot 2, POV blur insert, 1.0s: Through his blurred view, the dark-brown hand clue on the ground seems to hold a small ancient silk fragment.
Shot 3, crawling close-up, 1.2s: Old San painfully crawls toward it, breath shallow, fingers scraping dirt.
Shot 4, hand-object insert, 1.2s: He pries the ancient silk fragment from the stiff hand clue. Keep it small and readable, not graphic.
Shot 5, sleeve insert, 1.0s: He pushes the silk fragment into his sleeve and presses the fabric closed.
Shot 6, poisoned face close-up, 1.1s: His hearing fades; his eyes are cloudy, face cold and gray, but the decision is complete.
Shot 7, sound reaction, 1.0s: A faint clicking-croaking sound returns. Old San barely lifts his head, confused and afraid.
Shot 8, final reveal, 2.5s: A huge partial eyeless face lowers from above into the frame, empty eyes staring down at him. Old San is tiny below it, already too weak to react fully.

Lighting: Very low moonlight, most of the forest black. The second face is only partially lit from above, not fully revealed.
Do not show a full body for the second entity. Do not make the cloth fragment huge. Do not add extra monsters.
```
