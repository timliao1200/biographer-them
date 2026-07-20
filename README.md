# 壁爐邊 · 你眼中的他（Biographer-Them）

> **用 Walter Isaacson 的方法，陪你把另一個人的故事寫成一本書。**
>
> A Claude Code Skill that channels Walter Isaacson to help you write a biography of someone else — a parent, a partner, a mentor, a friend.

---

## What This Is

`biographer-them` 是 [Fireside Biographer 家族](https://github.com/timliao1200/biographer-me) 的**他傳版**。

- 自傳版 `biographer-me`：Isaacson 訪談你，你是主角
- **他傳版（這個）：** Isaacson 教你怎麼寫**另一個人**——你的父親、母親、伴侶、恩師、朋友

**這不是幫別人寫官方傳記。這是幫你把「你眼中的他 / 她」寫成一本書。**

---

## Who It's For

- **子女想幫父母留下故事**（最普遍）
- **害怕失去父母的人**（「怕來不及」）
- **想真正認識父母的成年子女**
- **失去親人後想告別、想理解的人**
- **想留下家族記憶給下一代的人**

---

## Two Paths · B1 vs B2

**Phase 0 就會判斷你走哪條路：**

### B1 · Memory Path（主角無法對話）
- 適用：主角過世 / 失智 / 距離太遠 / 關係破裂
- 資料來源：**你自己的記憶** + 家人口述 + 老照片 + 遺物
- Isaacson 化身幫你：分辨真實 / 聽說 / 想像 / 不知道
- 產出：《我眼中的他》——含大量「我不知道」的誠實模糊

### B2 · Interview Path（主角還在，但不用 AI）
- 適用：父母活著、能對話，但不會用 AI
- 資料來源：**你帶訪談腳本回家問主角本人**，回來給 AI 整理
- Isaacson 化身幫你：設計訪談問題、教你破冰、追細節、處理拒絕
- 產出：《爸爸口述、我筆錄》——含大量逐字對話

### 混合路徑
- 常見情境：主角部分能對話（失智初期能講童年、不能講最近）
- 兩條路徑並進，同一本書兩種資料來源並存
- **傳記倫理：清楚標記每段內容的來源**

---

## The 7-Phase Flow

| Phase | Name | What Happens |
|-------|------|-------------|
| **0** | Warm Welcome + 分岔 | 認識用戶、認識主角、決定 B1 / B2 |
| **1** | Understanding Them · 認識地形 | 主角來自哪裡（透過你的眼睛） |
| **2** | Turning Points · 找決定性瞬間 | 主角一生 5-7 個「沒發生會完全不同」的時刻 |
| **3A** | Memory Dive（B1） | 用你的記憶挖每個瞬間 + 標記真實/聽說/想像 |
| **3B** | Interview Script（B2） | 產出「你回家問他這幾題」的具體腳本 |
| **4** | Light & Shadow + Projection | 主角的光影 + 你對他的投射 |
| **5** | Outline · 拆章節 | 主題句（他的）+ 主題句（你們關係的） |
| **6** | Writing · 寫章節 | 標記真實/聽說/推測/不知道 |
| **7** | Share · 交出去 | 給誰讀？主角本人？下一代？ |

**跨 session 記憶：** 每次對話結束，AI 會把進度、主角資訊、資料來源分類寫進 `session/state.md`。

---

## What Makes This Different

### 1. 誠實的模糊，勝過假裝的全知

Isaacson 寫 Jobs 傳訪談 40+ 次，還是有不知道的地方。他標記出來。**你也一樣。**

不編。不假裝。「他當時可能想 X」和「他當時想 X」是兩個世界。

### 2. 這本書寫的其實是「你們」

用戶寫的不只是父親——是**「兒子筆下的父親」**。你也會在書裡出場。

這反而讓書有靈魂——因為它不是單面像，是雙人肖像。

### 3. 傳記倫理

書裡每段內容都會標記：
- `[真實]` 我親眼看到
- `[聽說]` 我從家人聽來
- `[推測]` 我合理推測
- `[不知道]` 這裡有一個空白，我坦承

**這種標記反而讓讀者信任這本書。**

---

## Installation · Works With Any AI Agent

### Universal Install（推薦 · 適用所有 AI Agent）

打開你的 AI Agent（**Claude Code、Codex、或其他**），貼這段：

```
請幫我從 GitHub 安裝這個 Skill：
https://github.com/timliao1200/biographer-them

無論你是 Claude Code、Codex 還是其他 AI Agent，請按以下步驟：

1. 找到你自己的 skills 目錄位置
   （Claude Code 通常在 ~/.claude/skills/；
    Codex 通常在 ~/.codex/skills/；
    其他 agent 依你的規範）

2. 用 git clone 把 repo 抓到那個目錄

3. 讀取裡面的 SKILL.md 跟 README.md，
   如果你的 skill 系統需要不同格式（例如 JSON manifest），
   請自動幫我轉換 —— 內容是標準 markdown + YAML frontmatter，
   任何 AI 都能讀

4. 驗證你能觸發它

5. 完成後告訴我：
   - 它裝在哪裡了
   - 我可以怎麼觸發它（用你 agent 的方式）
   - 準備好之後，我們就開始使用它
```

### Manual git clone（工程師）

依你的 AI Agent 選路徑：

```bash
# Claude Code
git clone --depth 1 https://github.com/timliao1200/biographer-them.git ~/.claude/skills/biographer-them

# Codex
git clone --depth 1 https://github.com/timliao1200/biographer-them.git ~/.codex/skills/biographer-them

# 其他 AI Agent · 依你的 skills 目錄規範
```

---

## Compatibility · 通用性說明

這個 Skill 使用 **標準 markdown + YAML frontmatter**——最開放、最通用的 skill 格式。

**已知支援：**
- ✅ Claude Code（`~/.claude/skills/`）
- ✅ Codex by OpenAI（`~/.codex/skills/`）

**理論支援（因為格式通用）：**
- 任何能讀 markdown SKILL.md 的 AI Agent
- 未來的 skill 系統
- 自訂 agent 框架

如果你的 agent 使用不同格式（例如 JSON manifest），請告訴你的 agent：**「請把這份 SKILL.md 轉成你需要的格式」**——大部分現代 AI 都能自動轉換。

---

## Usage

安裝完成後，對 Claude 說：

- 「我想寫我父親 / 母親的傳記」
- 「幫我寫我爸 / 我媽的一生」
- 「我怕來不及，想在父母走之前留下他們的故事」
- 「壁爐邊 · 你眼中的他」
- `/biographer-them`

Claude 會化身 Isaacson，從 Phase 0 開始問你：**「你想寫的是誰？」**

---

## File Structure

```
biographer-them/
├── SKILL.md                             # Isaacson persona + 7-phase state machine + B1/B2 分岔
├── README.md                            # 這份檔
├── LICENSE                              # MIT
├── frameworks/
│   ├── isaacson/                        # Isaacson 靈魂（跟 biographer-me 共用）
│   │   ├── method.md
│   │   ├── show-dont-tell.md
│   │   ├── light-and-shadow.md
│   │   ├── quotes.md
│   │   └── them-specific.md             # 【他傳專屬】誠實的模糊 + 投射處理
│   ├── phases/                          # 7 階段（他傳版）
│   │   ├── phase-0-welcome-them.md      # B1/B2 分岔關鍵
│   │   ├── phase-1-terrain-them.md
│   │   ├── phase-2-turning-points-them.md
│   │   ├── phase-3a-memory-dive.md      # B1 路徑
│   │   ├── phase-3b-interview-script.md # B2 路徑
│   │   ├── phase-4-projection-truth.md  # 光與影 + 投射
│   │   ├── phase-5-outline-them.md
│   │   ├── phase-6-writing-them.md      # 標記真實/聽說/推測/不知道
│   │   └── phase-7-share-them.md        # 給主角讀？
│   └── writing/
│       ├── chapter-templates.md
│       └── interview-script-templates.md  # 【他傳專屬】B2 訪談腳本模板
├── session/
│   └── STATE-TEMPLATE.md
├── output/
│   └── .gitkeep
└── examples/
    ├── b1-example.md
    └── b2-example.md
```

---

## Related Skills

Part of the **Fireside Biographer** family:

- **[`biographer-me`](https://github.com/timliao1200/biographer-me)** — 自傳版
- **`biographer-them`（你在這裡）** — 他傳版（B1/B2 雙路徑） 🕯️

---

## Sources

方法論基於：
- Lex Fridman Podcast #395 with Walter Isaacson
- NEH Jefferson Lecture (Isaacson)
- YouTube《Walter Isaacson's Writing Rules》
- Isaacson's books: *Steve Jobs*, *Elon Musk*, *Einstein*, *Leonardo da Vinci*, *Benjamin Franklin*, *The Code Breaker*

**這個 Skill 不是官方授權，是對 Isaacson 公開方法論的致敬與應用。**

---

## Contributing

歡迎 PR。特別歡迎：
- 更多訪談腳本模板（不同情境：跟長輩、跟關係緊張的家人、跟摯友）
- 傳記倫理案例討論
- 華人家庭情境的破冰技巧

---

## License

MIT License. See `LICENSE`.

---

## Author

Made with 🕯️ by [Tim Liao](https://github.com/timliao1200)（廖敬提）

---

## Final Words

> *"A biography is a bridge — one person's attempt to reach another, knowing they'll never fully cross."*
>
> 傳記是一座橋——一個人試圖走向另一個人，明知永遠不會完全走到。

**這個 Skill 存在的意義：讓每一個「怕來不及」的人，都能在來得及的時候，開始這座橋。**
