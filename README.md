# 2026 大阪家族旅行（11/4–11/9）公開版網站

線上網址：https://mingmingcapital-gif.github.io/2026-osaka-trip/

## 內容
- `index.html`：總覽（每日卡片、注意事項、機票、指南）。
- `d0.html`–`d5.html`：每日行程。上方有重點摘要、目錄、本日景點卡片。
- `p/*.html`：景點頁與指南頁（入境、參拜禮儀、臨空城、唐吉訶德、帝王蟹）。上方有麵包屑。
- `data/osaka_spots_D0–D5.csv / .kml`：每日地點，可匯入 Google 我的地圖。
- `assets/site.css`：樣式。純靜態，沒有 JavaScript。

## 產生方式
1. 從 Notion 匯出頁面 Markdown 到 `../site_src/notion/`。
2. 執行 `python3 ../site_src/build_site.py`（只讀來源，只寫這個資料夾）。
3. 推送前執行 `../site_src/pii_scan.sh .` 與 `gitleaks detect --source . --redact`，兩個都要通過。

## 公開版刻意排除的資料
- 機票與訂房的代碼、護照資料、保單號碼、緊急聯絡資料、家人電話與 email。
- 個人姓名（改成「先行者」）。
- D0 與 D1–D3 飯店名稱、地址、房型與訂房細節（改成「D0 飯店」「市區飯店」）。
- 地圖連結中指向飯店的目的地（改成日本橋站）。
- CSV/KML 中的住宿列；完整版 `osaka_spots.csv/.kml` 不公開。
- 舊行程備份頁、Notion 內部連結、圖片（版權因素，只留說明文字）、寄給飯店的信件草稿。

資料以 Notion 為準；本網站是 2026-11-03 的版本。
