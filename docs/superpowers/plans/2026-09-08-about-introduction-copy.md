# About Introduction Copy Refresh Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the homepage's two introductory paragraphs with the approved polished, professional, and lightly playful biography.

**Architecture:** This is a copy-only change in the existing Jekyll Markdown homepage. Replace lines 23–25 as one atomic edit, preserving the surrounding front matter, Liquid template code, page sections, facts, and link destinations.

**Tech Stack:** Jekyll, Markdown, Liquid

## Global Constraints

- Preserve every existing biographical fact and URL.
- Keep the tone professional enough for an academic homepage.
- Include exactly one playful line: “because even the most capable agents could use a good memory.”
- Do not modify content outside the two introductory paragraphs.

---

### Task 1: Refresh the About Introduction

**Files:**
- Modify: `_pages/about.md:23-25`
- Reference: `docs/superpowers/specs/2026-09-08-about-introduction-copy-design.md`

**Interfaces:**
- Consumes: The existing Jekyll page structure and approved copy in the design specification.
- Produces: Two valid Markdown paragraphs rendered at the top of the homepage.

- [ ] **Step 1: Replace the two introductory paragraphs**

Use this exact copy:

```markdown
Since September 2024, I have been pursuing a master's degree at the [School of Computer Science](https://cs.fudan.edu.cn/) of [Fudan University](https://www.fudan.edu.cn/). As a member of the [FudanNLP Lab](https://nlp.fudan.edu.cn/), I am co-advised by Prof. [Xuanjing Huang (黄萱菁)](https://xuanjing-huang.github.io/) and Associate Prof. [Tao Gui (桂韬)](https://guitaowufeng.github.io/). Previously, I received my bachelor's degree from Fudan University in June 2024 under the supervision of Prof. [Xuanjing Huang](https://xuanjing-huang.github.io/).

My research journey has taken me from **model reasoning** and **reward modeling** to my current focus on **agent memory**. Broadly, I am interested in building agents that can reason reliably, learn from feedback, and remember what truly matters—because even the most capable agents could use a good memory. If any of these topics resonate with you, feel free to reach out via [email ✉️](mailto:liusc2020@gmail.com) or [RedNote (小红书)](https://xhslink.com/m/CWTAntd2dt)—I am always happy to exchange ideas, explore potential collaborations, or simply chat about the latest twists and turns in AI research! 👏🏻
```

- [ ] **Step 2: Verify required content and links**

Run:

```bash
rg -n "Since September 2024|most capable agents could use a good memory|mailto:liusc2020@gmail.com|xhslink.com/m/CWTAntd2dt" _pages/about.md
```

Expected: The refreshed biography appears on lines 23 and 25, including both contact links and the single playful sentence.

- [ ] **Step 3: Check Markdown whitespace and scope**

Run:

```bash
git diff --check
git diff -- _pages/about.md
```

Expected: No whitespace errors, and the diff changes only the two introductory paragraphs.

- [ ] **Step 4: Commit the implementation**

```bash
git add _pages/about.md
git add -f docs/superpowers/plans/2026-09-08-about-introduction-copy.md
git commit -m "update about introduction"
```
