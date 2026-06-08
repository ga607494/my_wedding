# 葉政昇 ❤ 謝欣汝 · 婚禮邀請函

純靜態 H5 婚禮邀請函，所有資源（圖片、字體、音樂、CSS）已本地化，可直接部署到 GitHub Pages。

## 本地預覽

GitHub Pages 與瀏覽器的字體 / 圖片需透過 HTTP 載入（`file://` 會有限制），請用任一本地伺服器：

```bash
# Python（內建）
python3 -m http.server 8765
# 然後開 http://localhost:8765

# 或 Node
npx serve .
```

## 部署到 GitHub Pages

1. 建一個新的 GitHub repo，把本資料夾所有檔案推上去：
   ```bash
   git init && git add -A && git commit -m "wedding invitation"
   git branch -M main
   git remote add origin https://github.com/<你的帳號>/<repo-name>.git
   git push -u origin main
   ```
2. repo → **Settings → Pages** → Source 選 **Deploy from a branch** → Branch 選 `main` / `/ (root)` → Save。
3. 等 1–2 分鐘，網址會是 `https://<你的帳號>.github.io/<repo-name>/`。

> `.nojekyll` 已包含，確保 GitHub Pages 原樣提供所有檔案。

## 結構

```
index.html            # 單頁邀請函（含 inline CSS/JS）
assets/
  img/                # 婚紗照、裝飾圖片
  font/               # 自訂字體（標題藝術字 / 思源宋體等）
  audio/bgm.mp3       # 背景音樂
  css/app.css         # 排版樣式（.ele-* 絕對定位系統）
  css/animate.min.css # animate.css
```

## 自訂

- 換照片：替換 `assets/img/` 內檔案，或改 `index.html` 中對應 `<img src>`。
- 改文字：搜尋 `index.html` 內的姓名 / 日期 / 地址直接修改。
- 改倒數目標時間：搜尋 `2026-10-31T11:30:00+08:00`。
- 換音樂：替換 `assets/audio/bgm.mp3`。
