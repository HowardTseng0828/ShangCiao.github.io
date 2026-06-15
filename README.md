# 上巧工程行 - 形象網站

這是一個為「上巧工程行」設計的形象網站，展示公司提供的服務與聯絡資訊，讓用戶能快速了解服務內容及聯繫方式。

## 技術架構

- HTML5（語意化標籤、單頁形象網站）
- 純自訂 CSS3（CSS Grid + Flexbox 響應式排版，適配桌面、平板、手機）
- 設計風格：亮色乾淨專業業者風（白底 + 信任藍主色 + 暖橘點綴）
- Font Awesome 圖示、Google Fonts（Noto Sans TC / Rajdhani）
- 無框架、無 build 步驟、無外部 JS 套件（僅少量原生 JS 處理手機選單）

## 本機執行

直接用瀏覽器開啟 `index.html` 即可，無需額外安裝套件或伺服器。

```bash
# 或使用 VS Code Live Server 套件預覽
```

## 線上瀏覽

網站部署於 **Cloudflare Pages**（部署步驟見 [DEPLOY.md](DEPLOY.md)）。

## 專案結構

```
ShangCiao.github.io/
├── index.html          # 主頁面
├── css/
│   └── style.css       # 自訂樣式（亮色設計 token + 各元件）
├── images/             # 圖片資源
├── _headers            # Cloudflare Pages 快取與安全標頭設定
└── DEPLOY.md           # Cloudflare Pages 部署步驟（超新手版）
```
