# 部署到 Cloudflare Pages（超新手版）

這個網站是純靜態網站（只有 HTML + CSS + 圖片，沒有後端、沒有 build 步驟），
所以搬到 Cloudflare Pages 非常簡單。下面照步驟做就好。

---

## 做法：接上 GitHub，之後 push 就自動更新

> 這個做法的好處：程式碼還是放在 GitHub，
> 你以後只要 `git push`，Cloudflare 就會自動重新部署，不用手動上傳。

### 步驟

1. 先把目前的改動推上 GitHub（在這個資料夾開終端機）：
   ```bash
   git add .
   git commit -m "2026-06-15 1.【UI】改為亮色乾淨專業風 2.【部署】改用 Cloudflare Pages"
   git push
   ```

2. 開 Cloudflare 後台 → 左邊選單找 **Workers & Pages** → 按 **Create application** → 選 **Pages** 分頁 → **Connect to Git**。

3. 第一次用要先授權 Cloudflare 連到你的 GitHub，授權後選這個 repo：
   `HowardTseng0828/ShangCiao.github.io`

4. **Build settings（建置設定）這樣填**（重點：這站沒有 build，全部留空）：
   - **Framework preset**：`None`
   - **Build command**：留空（什麼都不填）
   - **Build output directory**：填 `/`（根目錄，因為 `index.html` 就在最外層）

5. 按 **Save and Deploy**，等一下下，Cloudflare 會給你一個網址，像是：
   `https://shangciao-github-io.pages.dev`

6. 打開那個網址，確認網站正常 → 完成！以後 `git push` 就會自動更新。

---

## 之後想綁自己的網域（例如 www.上巧.com）

在 Cloudflare Pages 專案裡 → **Custom domains** → **Set up a custom domain**，
照畫面把網域加進去就好（如果網域本來就在 Cloudflare 管理，會自動設定 DNS）。

---

## 補充說明

- `_headers` 檔：Cloudflare Pages 會自動讀，用來設定圖片快取和基本安全標頭，你不用動它。
- 原本的 GitHub Pages 可以保留也可以關掉；兩邊不衝突。
  要關的話：GitHub repo → **Settings** → **Pages** → Source 改成 `None`。
