# 视频知识库说明

本目录只存放跨集、跨项目可复用的方法论和规则。具体角色、场景、道具、图片路径和生成状态放在 `assets/`，单集产物放在 `output/epXX/`。

## 目录分工

```text
knowledge/
  cinematography/         摄影语言：景别、机位、构图、画面地理、运镜
  performance/            动画表演：表情、呼吸、姿态、重心、手部、下肢
  editing_and_coverage/   剪辑与镜头覆盖：coverage pattern、reaction、POV、montage
  ai_generation/          AI 生成工艺：生成方式决策、模型渲染手册、实测复盘
    modes/                具体生成模式：全能、分镜图、首尾帧、行为起始帧
  templates/              选读镜头模板库
```

## 使用规则

1. 先确定剧情目的，再查对应知识库，不为了套术语改剧情。
2. 同类规则只维护在一个专业目录里：摄影归 `cinematography/`，表演归 `performance/`，剪辑与 coverage 归 `editing_and_coverage/`，AI 生产工艺归 `ai_generation/`。
3. 库文件是检索工具，不是 prompt 原文仓库。最终提示词只保留当前镜头真正需要的规则。
4. 本集特殊规则写入 `output/epXX/cinematography.md` 或对应阶段产物，不回灌到通用知识库，除非它已经被多次验证为长期方法。

## 文件索引

- `cinematography/shot_and_camera_language.md`：景别、机位、构图、画面地理关系、运镜类型与运镜选择。
- `performance/performance_signal_library.md`：表情、呼吸、姿态、重心、手部、下肢等可见表演信号。
- `editing_and_coverage/coverage_scene_pattern_library.md`：master、coverage、reaction、POV、montage 等剪辑与镜头组织方式。
- `ai_generation/generation_decision_library.md`：状态型/事件型、单镜头/multi-shot、全能模式、首尾帧、行为起始帧、分镜图驱动的选择。
- `ai_generation/modes/omnipotent_mode.md`：全能模式专属规则，多图参考、`@` 锚定、上传顺序。
- `ai_generation/modes/storyboard_frame_mode.md`：分镜图驱动专属规则，图内人物指认、动作桥、防 PPT。
- `ai_generation/modes/start_end_frame_mode.md`：首尾帧专属规则，起点/终点过渡与落点控制。
- `ai_generation/modes/action_start_frame_mode.md`：行为起始帧专属规则，人物已在动作中的起始图。
- `ai_generation/model_renderer_playbooks.md`：Seedance / Kling 等模型渲染手册。
- `ai_generation/video_field_test_findings.md`：真实生成测试的成功条件、失败条件和修正方向。
- `templates/cinematic_shot_templates.md`：选读镜头模板库，需要风格化镜头时使用。
