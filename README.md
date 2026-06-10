# ivanchen114.github.io

個人工具櫃入口頁。線上:https://ivanchen114.github.io/

## 新增 / 修改工具

打開 `index.html`,找到 `const tools = [` 這段,複製任一個物件貼下去改即可。每個物件需要這六個欄位:

```js
{
  title: "工具名稱",
  desc: "一行說明",
  url: "https://...",
  tag: "vercel",        // vercel | apps-script | local | gh-pages
  status: "active",     // active(🟢) | beta(🟡) | broken(🔴)
  category: "教學網站"   // 自由命名,新分類會自動出現
}
```

可選欄位:`icon`(專屬 SVG 圖示名)、`dataUrl`(原始資料連結,支援字串或陣列)、`codeUrl`(原始碼連結)。

完全不用動 HTML、CSS、其他 JS。改完存檔即可。同分類內的卡片會依點擊次數自動排序(常用的浮上來);「最後更新」日期自動抓 GitHub 最後 commit 時間,不用手動改。

## 部署

```bash
./deploy.sh              # 預設 commit 訊息「更新工具清單」
./deploy.sh "改了什麼"    # 自訂訊息
```

腳本會自動:pull repo → 複製 index.html / README.md 到 `~/Documents/Ivanchen114.github.io` → commit → push。不要再手動 cp。

推上去後 30 秒~2 分鐘 GitHub Pages 會自動部署。打開網址用 `Cmd+Shift+R` 強制重整避免抓到舊快取。

## 同 repo 其他檔案

- `draw.html` — 抽籤系統,網址 `https://ivanchen114.github.io/draw.html`

## 鍵盤快捷鍵

- `/` — 聚焦搜尋框
- `Enter`(在搜尋框內)— 直接開啟畫面上第一個結果
- `Esc` — 清空搜尋並失焦
