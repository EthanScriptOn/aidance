# Output

Every episode folder should contain the smallest set of files needed to keep multi-episode generation stable:

```text
output/epXX/
├── asset_manifest.md    本集用哪些已锁资产、需要哪些新增资产或变体
├── episode_spine.md     本集拆成哪些可生成片段，每段状态如何变化
├── prompt_cards.md      最终可直接粘贴到视频模型的提示词卡
└── test_notes.md        实测结果、失败原因、可复用经验
```

`output/` is not for department reports.

Keep only production files that answer one of these questions:

- 本集用什么？
- 本集拍哪些片段？
- 每个片段怎么生成？
- 生成效果如何回写？

If a file does not help answer those questions, it should not live here.
