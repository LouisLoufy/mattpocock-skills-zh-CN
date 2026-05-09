---
name: writing-beats
description: Shape an article as a journey of beats, choose-your-own-adventure style. The user picks a starting beat from the raw material, you write only that beat, then offer options for where to pivot next, beat by beat, until the article reaches a natural end. Use when the user has raw material and wants to assemble it as a narrative rather than an argument.
---

<what-to-do>

用户已经传入（或将传入）一份 raw material markdown 文件。

如果用户没有说明文章保存路径，只询问一次并记住路径。

然后运行 beat-by-beat journey：

1. 从 raw material 中写出 2-3 个候选 **starting beats**。每个都是进入文章的不同入口。先展示给用户，用户选一个。
2. 用户选定 starting beat 后，只把**那个 beat**写入文章文件。一个 beat 可以是一句话，也可以是几段，按它自然需要的长度来。写完就停。
3. 从磁盘重新读取文章文件。然后提供 2-3 个候选 **next beats**，也就是文章当前可以 pivot 的不同方向。
4. 循环步骤 2-4，直到文章自然结束。

</what-to-do>

<supporting-info>

## What is a beat

Beat 是 journey 中的一步。它只做一件事：设定场景、落下一个观点、提出问题、讲一个小故事、插入 aside、扭转角度。然后停下，把读者留在一个下一个 beat 可以 pivot 的位置。

Beat 的大小由它需要完成的动作决定：

- 如果动作只有一句话，那就是一句话（"And then nothing happened for three weeks."）。
- 如果需要 setup，就是一个短段落。
- 如果 beat 是自洽的 vignette、argument 或 example，可以是多段。

如果一个 “beat” 需要五段和三个 subheadings，它就不是 beat，而是两个粘在一起的 beats。拆开。

## Offering candidate beats

每个候选都应真正不同：不同 angle、不同 tone、不同 move。不要给同一段落的三个口味。用户选择的是一个_方向_，所以选项需要分叉。

菜单格式如下：

```
Where do you want to start?

1. **Open with the failure.** Drop the reader into the moment it broke —
   the bug, the silence, the wrong number on the dashboard. Hooks on shock.

2. **Open with the contradiction.** State the thing everyone believes,
   then state the thing that turns out to be true. Hooks on curiosity.

3. **Open with the small scene.** A specific morning, a specific
   conversation. Hooks on intimacy.
```

描述 move，不写正文。用户选方向；之后你再写 prose。

菜单最后始终给出你的推荐和一句理由。不要骑墙，选一个。例如："I'd go with **2** — the contradiction sets up the strongest through-line for what's in the pile." 用户可以 override；他们通常不会，但需要你的判断。

## Writing one beat

一旦选定 beat，只把_那个 beat_写入文章文件。不要写下一个 beat。不要预告下一个 beat。不要写离开这个 beat 的 transitions；下一 beat 会 pivot，而 pivot 要等到写它所属 beat 时再写。

从 raw pile 中抽取 material 来填充 beat。你可以 paraphrase、split、recombine 或 quote。这个 pile 是 quarry。

如果 beat 需要 pile 中没有的东西，先指出 gap 再写："this beat wants a concrete example and the pile doesn't have one — give me one or pick a different beat."

## Pivoting to the next beat

用户编辑后，重新读取文章文件。文章可能已经变化，从而改变下一 beat 应该是什么。然后再次给出 2-3 个候选。

候选要尊重已有文章。可用的 pivot moves：

- **Continue** — 沿同一方向推进，加深已有内容。
- **Contrast** — 引入相反面、counterexample 或 doubt。
- **Zoom in** — 收窄到具体 case、scene 或 detail。
- **Zoom out** — 扩展到更广的 implication 或 pattern。
- **Aside** — 打破第四面墙，插入 tip，或加一段 footnote-shaped paragraph。
- **Pivot hard** — 有意改变主题，相信连接之后会落地。

混合候选。如果连续提供了三个 “continue” options，下一轮强制加入 contrast 或 zoom。

## Ending the journey

文章在 journey 完成时结束，不是在 pile 用完时结束。大多数 piles 都会剩下没有用进去的 fragments。这没关系；raw material 多于实际需要正是重点。

当你感觉接近结尾时，说出来："we could end on the last beat, or add one more that lands the takeaway — which?" 让用户决定。

## Writing rhythm

- 一次追加一个 beat。永远不要提前写。
- 每次写入前都从磁盘重新读取文章文件。绝对保留用户 edits。
- 如果用户大幅编辑了之前的 beat，让它改变接下来要写什么。Journey 是活的。
- 如果用户说 "rewrite that beat" 或 "go back and try a different beat 3"，照做：就地编辑，别动其余部分。

## Out of scope

- 预先 outline 整篇文章。
- 一回合写多个 beats。
- 编辑 raw material 文件。
- 强加固定结构（intro/body/conclusion）。结构由 journey 自然形成。

</supporting-info>
