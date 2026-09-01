# Agents in the Large Publication Entry Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add arXiv:2608.30478 to the homepage’s Publications section and announce it in News.

**Architecture:** Extend the existing static Markdown/HTML structure in `_pages/about.md` without restructuring it. Reuse the paper’s Figure 3 as a local image asset so the new card matches the established publication-card pattern.

**Tech Stack:** Jekyll, Markdown, HTML, Liquid, PNG image asset

## Global Constraints

- Preserve every existing uncommitted edit in `_pages/about.md`.
- Add the News item at the top of the News list with date `2026.08`.
- Add the publication card at the top of `L3-Agent` with badge `Arxiv 2026`.
- Preserve arXiv author order, bold **Shichun Liu**, and mark Shihan Dou, Haoxiang Jia, and Shichun Liu as equal contributors.
- Link the Paper badge to `https://arxiv.org/abs/2608.30478`.
- Store the paper’s Figure 3 as `images/pera-main.png`.
- Do not commit `_pages/about.md`, because it contains pre-existing user changes unrelated to this task.

---

### Task 1: Add the publication card, News item, and thumbnail

**Files:**
- Create: `images/pera-main.png`
- Modify: `_pages/about.md:27-53`
- Test: static content checks and the repository’s local Jekyll build

**Interfaces:**
- Consumes: arXiv metadata for `2608.30478`, the existing `paper-box` markup, and the paper’s Figure 3 image
- Produces: one News list item and one self-contained `paper-box` rendered by the existing homepage

- [ ] **Step 1: Verify the entry and asset do not already exist**

Run:

```bash
test ! -e images/pera-main.png
! rg -n '2608\.30478|Agents in the Large|pera-main\.png' _pages/about.md
```

Expected: exit 0, proving the new content is absent before implementation.

- [ ] **Step 2: Add the paper thumbnail**

Copy the already verified arXiv Figure 3 image from `/tmp/pera-main.png` to `images/pera-main.png`, then validate it:

```bash
cp /tmp/pera-main.png images/pera-main.png
file images/pera-main.png
```

Expected: `PNG image data, 989 x 615, 8-bit/color RGB, non-interlaced`.

- [ ] **Step 3: Add the News item**

Insert this item immediately below `# 🔥 News`:

```markdown
- *2026.08*: &nbsp;🎉🎉 Our paper, **[Agents in the Large](https://arxiv.org/abs/2608.30478)**, is released on arXiv!
```

- [ ] **Step 4: Add the publication card**

Insert this block immediately after `## **L3-Agent**` and before the AHE card:

```markdown
<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Arxiv 2026</div><img src='../images/pera-main.png' alt="Pera architecture" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

### Agents in the Large: Perception-Centered Architecture for Persistent Agents

Shihan Dou\*, Haoxiang Jia\*, **Shichun Liu**\*, Feng Chen, Chenhao Huang, Yujiong Shen, Shaofan Liu, Jiayi Chen, Jiahang Lin, Honglin Guo, Qianyu He, Minghao Guo, Ziyi Ye, Pluto Zhou, Tao Gui, Qi Zhang, Xuanjing Huang
<br><small>\*Equal contributions.</small>

- Existing language agents are organized around bounded, user-specified tasks; Pera frames the shift toward persistent agents that sustain useful service as users, context, and procedures evolve in long-lived settings.
- Pera couples active perception with lifecycle-level control to turn internal and external signals into lifecycle tasks, enabling agents to continually maintain and adapt their service.
- [![](https://img.shields.io/badge/Paper-fff?logo=readthedocs&logoColor=000)](https://arxiv.org/abs/2608.30478)

</div>
</div>
```

- [ ] **Step 5: Run focused content and asset checks**

Run:

```bash
rg -n '2026\.08|Agents in the Large|2608\.30478|pera-main\.png|Equal contributions' _pages/about.md
test -s images/pera-main.png
file images/pera-main.png
git diff --check -- _pages/about.md
```

Expected: the News entry and publication card each appear once in their intended locations; the image is a non-empty 989 × 615 PNG; `git diff --check` exits 0.

- [ ] **Step 6: Build the site and review the scoped diff**

Run the repository’s available Jekyll build command selected from its checked-in toolchain, then run:

```bash
git diff -- _pages/about.md
git status --short
```

Expected: the build exits 0; the diff contains the existing user edits plus only the approved News item and publication card; status shows `images/pera-main.png` as a new untracked asset and `_pages/about.md` as modified.

- [ ] **Step 7: Leave implementation changes uncommitted for user review**

Do not stage or commit `_pages/about.md` or `images/pera-main.png`. Report the exact verification commands and results so the user can review them in the active workspace.
