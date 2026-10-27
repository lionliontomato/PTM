# 地瓜瓜の存鑽與存歌 🍠

此網站保留參考站 TO 的五欄資料表、搜尋、彩色欄位及版權頁架構，主題改成粉紅色日本少女風。可直接部署至 GitHub Pages。

## Google 試算表
https://docs.google.com/spreadsheets/d/1_JidetnwNCBcLctoIMecD88owHZV1luItxt_0xm10Oc/edit?usp=sharing

- 預設讀取第一個工作表（`script.js` 內 `SHEET_GID = '0'`）。請依你的實際工作表 gid 調整。
- A～E 欄依序：存鑽老闆、存鑽數量、存歌數量、存爆數量、總數。
- L 欄（第 12 欄）為設定名稱；M 欄（第 13 欄）為設定內容。例如 L1=`網站標題`、M1=`地瓜瓜の存鑽與存歌`；L2=`網站小標題`、M2=`你的副標題`。
- **可編輯 L／M** 指的是擁有試算表編輯權限的人可直接在 Google Sheets 編輯這兩欄；網頁重新讀取時自動同步。此純靜態網站不開放訪客寫入試算表。
- Google Sheet 必須允許「知道連結的使用者可以檢視」才能以匿名方式讀取。
- 若 L／M 沒有設定標題，會使用預設標題；若沒有小標題則保持空白，不閃出舊內容。
- 網頁每次載入向 Google 重新請求資料（含防快取參數），若讀取失敗只顯示錯誤，不顯示舊資料。Google 端的更新傳播仍可能有短暫延遲。

## GitHub Pages

1. 解壓縮 ZIP，將**所有檔案**放在儲存庫根目錄（`index.html`, `script.js`, `style.css`, `copyright.html`, `favicon.svg`, `sakura-pink.png`, `.nojekyll`）。
2. GitHub Repository → Settings → Pages → Deploy from a branch → main → /(root) → Save。
3. 等待部署後打開新網址測試表格資料、L／M 文字設定與手機版。

## 限制

已完成靜態語法、欄位映射、ZIP 結構等檢查；由於無法在此環境直接取得新試算表內容，**未能做真實線上 Google Sheets 讀取驗證**。如你的資料位於其他分頁或不是標準 A～E 與 L／M 配置，須調整 `SHEET_GID` 或欄位映射。
