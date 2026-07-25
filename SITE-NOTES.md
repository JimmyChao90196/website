# 網站維護手冊 🛠️

> 這份筆記放在 repo 根目錄，會跟著 git 同步（Mac / Windows 都看得到），Hugo 不會把它發布到網站上。
> 網址：https://JimmyChao90196.github.io/

---

## 📁 檔案地圖 — 什麼東西在哪裡改

| 想改的東西 | 檔案 |
|---|---|
| 網站標題（分頁名稱、header 上的站名） | `config/_default/languages.en.toml` → `title` |
| 網站描述 / 副標（SEO + 部分版型顯示） | `config/_default/languages.en.toml` → `[params] description` |
| 作者名字 / 頭像 / bio / headline | `config/_default/languages.en.toml` → `[params.author]` |
| 社群連結（IG、FB、YouTube…） | `config/_default/languages.en.toml` → `[params.author] links` |
| 首頁內文段落 | `content/_index.md` |
| 首頁「最近更新」設定 | `config/_default/params.toml` → `[homepage]` |
| 最近更新要顯示哪些分類 | `config/_default/params.toml` → `mainSections` |
| 導航選單 / 下拉選單 | `config/_default/menus.en.toml` |
| 背景圖 | `config/_default/params.toml` + `assets/css/custom.css` |
| 配色 / 深淺色模式 | `config/_default/params.toml` → `colorScheme`、`defaultAppearance` |
| About 頁內容 | `content/about.md` |
| 各分類 / 文章內容 | `content/<分類>/<頁面>/index.md` |

---

## ✏️ 常見修改

### 1. 網站標題、描述
`config/_default/languages.en.toml`
```toml
title = "Jimmy Chao Learning Lab"          # 站名（分頁標題、header）

[params]
description = "FX breakdowns, Houdini notes, sculpting studies, and project writeups."
```

### 2. 作者資訊 + 社群連結（加 Instagram / Facebook）
`config/_default/languages.en.toml` 的 `[params.author]`：
```toml
[params.author]
name = "Jimmy Chao (Jun-Yu Zhao)"
email = "myname90196@gmail.com"
image = "https://avatars.githubusercontent.com/..."   # 頭像
headline = "iOS Engineer / FX Artist / Sculptor"
bio = "I sculpt, I code, I learn."
  links = [
    { github = "https://github.com/JimmyChao90196" },
    { linkedin = "https://www.linkedin.com/in/jimmy-chao-137aa2201/" },
    { link = "https://www.artstation.com/jimmy90196" },
    { youtube = "https://youtu.be/..." },
    # 👇 想加就加這兩行（把網址換成你的）
    { instagram = "https://instagram.com/你的帳號" },
    { facebook = "https://facebook.com/你的帳號" },
  ]
```
> 支援的平台很多（tiktok、threads、bluesky、mastodon、discord…），格式都一樣 `{ 平台名 = "網址" }`。完整清單在同一個檔案下方的註解裡。

### 3. 首頁內文
`content/_index.md` — 上面 `---` 之間是設定，下面是顯示的文字：
```markdown
---
title: "Learning Lab"
description: "..."
---

By day, I write iOS. After hours, I sculpt.

（這裡的文字就是首頁顯示的內文）
```

### 4. 首頁「最近更新」
`config/_default/params.toml`
```toml
mainSections = ["projects"]        # ← 決定哪些分類會進最近更新
                                   #   想加 anatomy：["projects", "anatomy"]

[homepage]
  showRecent = true               # 開/關最近更新
  showRecentItems = 3             # 顯示幾筆
  showMoreLink = true             # 「查看更多」按鈕
  showMoreLinkDest = "/projects/" # 按鈕連到哪
```
- **排序**：照每頁 front matter 的 `date:` 由新到舊。想讓某篇排前面就改它的 `date`。

### 5. 導航選單 / 下拉
`config/_default/menus.en.toml`。一個 `[[main]]` = 一個選單項目：
```toml
[[main]]
  name = "Anatomy"          # 顯示名稱
  pageRef = "anatomy"       # 連到哪個分類
  weight = 60               # 排序（數字小的在左）

[[main]]
  name = "Head"             # 下拉子項目
  parent = "Anatomy"        # ← 有 parent 就會變成 Anatomy 的下拉
  pageRef = "anatomy/head"
  weight = 10
```

### 6. 背景圖
兩個地方要一起改（首頁 + 其他頁）：
```toml
# config/_default/params.toml
defaultBackgroundImage = "img/rog-lightning-highway.png"
[homepage]
  homepageImage = "img/rog-lightning-highway.png"
```
```css
/* assets/css/custom.css 第 31 行 */
url("/img/rog-lightning-highway.png") center / cover no-repeat;
```
> 圖片檔放在 `assets/img/`。三個地方換成同一個檔名即可全站統一。

### 7. 配色 / 深淺色
`config/_default/params.toml`
```toml
colorScheme = "noir"            # 主題配色
defaultAppearance = "dark"      # 預設 dark 或 light
autoSwitchAppearance = true     # 跟隨系統
```

---

## ➕➖ 新增 / 刪除

### 新增一個頁面
1. 建資料夾：`content/<分類>/<頁面名>/`
2. 裡面放 `index.md`，開頭要有 front matter：
```markdown
---
title: "頁面標題"
date: 2026-07-25
description: "描述"
featureimage: "feature.webp"     # 卡片縮圖（放同資料夾）
tags: ["tag1", "tag2"]
---

內文…
```
3. 圖片放同一個資料夾，用 `![](檔名.webp)` 或 gallery 引用。

### 刪除一整個分類 / 頁面
1. 刪掉 `content/<分類>/` 整個資料夾
2. 到 `config/_default/menus.en.toml` 把對應的 `[[main]]` 選單項目刪掉
3. 若它在 `mainSections` 裡也要移除
4. 重新 build 部署 → 分類頁 / tag / category 會自動消失
> ⚠️ 光刪資料夾但沒刪 menu，選單會出現壞掉的連結。兩邊都要處理。

### 圖片排成網格（gallery）
在 `index.md` 裡用 gallery shortcode：
```markdown
{{< gallery >}}
  <img src="feature.webp" class="grid-w100" />
  <img src="a.webp" class="grid-w100 md:grid-w50" />
  <img src="b.webp" class="grid-w100 md:grid-w50" />
{{< /gallery >}}
```
- `grid-w100` = 整排寬、`grid-w50` = 半排（兩張一列）、`grid-w33` = 三張一列、`grid-w25` = 四張一列
- `md:grid-w50` = 平板以上才半排，手機自動變整排（RWD）

---

## 🔍 預覽（改東西時邊改邊看）

在終端機跑：
```powershell
hugo server --source C:\Users\user\Desktop\website
```
→ 瀏覽器開 **http://localhost:1313**（改檔案會即時自動重載）

- 關閉：終端機按 **`Ctrl + C`**
- 看草稿（`draft: true` 的頁面）：指令後面加 `-D`

> 預覽只有你自己看得到，跟線上網站無關。滿意後才跑「部署」。

---

## 🚀 部署（讓改動上線）

⚠️ **鐵則：任何機器開工前、部署前，先 `git pull`**（因為 Mac / Windows 交替使用）

```powershell
$site = "C:\Users\user\Desktop\website"
Set-Location $site

git pull origin main                          # ① 先同步
Get-ChildItem "$site\public" | Where-Object { $_.Name -ne ".git" -and $_.Name -ne ".gitattributes" } | Remove-Item -Recurse -Force
hugo --source $site                            # ② 重新 build

Set-Location "$site\public"                    # ③ 推 public（網站本體）
git add -A
git commit -m "Update site"
git push origin main

Set-Location $site                             # ④ 推外層（更新指標）
git add -A
git commit -m "Update content"
git push origin main
```
> Mac 上一樣，只是把 `$site` 換成 Mac 的路徑。

---

## 🧰 其他常用 git 指令

**換機器 / 開工前同步：**
```powershell
Set-Location "C:\Users\user\Desktop\website"
git pull origin main
```

**看目前狀態：**
```powershell
git status              # 改了什麼
git status -sb          # 精簡版，看領先/落後遠端
```

**本地改壞想丟掉、回乾淨：**
```powershell
git checkout -- .       # 丟掉所有未 commit 的改動
git clean -fd           # 刪掉多餘的新檔案（小心用）
```

---

## 🚨 疑難排解

### 網站推了，線上卻沒更新
GitHub Pages 偶爾不會自動觸發建置（例如 GitHub 當下伺服器出錯）。推一個空 commit 去戳它：
```powershell
Set-Location "C:\Users\user\Desktop\website\public"
git commit --allow-empty -m "Trigger Pages rebuild"
git push origin main
```
等 1–2 分鐘後硬重新整理瀏覽器（`Ctrl + Shift + R`）。

### push 被拒絕（rejected / behind）
代表另一台機器推過東西。先拉再推：
```powershell
git pull origin main
# （解決衝突，如果有的話）
git push origin main
```

### 圖片在線上是壞的
- 先確認 `public/.gitattributes` 裡有 `* binary`（防止 git 弄壞二進位檔）
- 通常是瀏覽器快取，硬重新整理 `Ctrl + Shift + R`

### 線上到底更新了沒？
看網站的 `Last-Modified` 時間戳，或用瀏覽器無痕視窗開，避開快取。

---

## 📌 重點速記

- 改**內容** → `content/`
- 改**設定**（標題、社群、首頁、選單、配色）→ `config/_default/`
- 改**全站樣式**（背景等）→ `assets/css/custom.css`
- 流程永遠是：**pull → 改 → hugo server 預覽 → 部署（build + push ×2）**
- 換機器 = 先 pull
