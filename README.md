# 🔐 Vault Pro - 智能金鑰守門員

Vault Pro 是一個基於 **GitHub Pages** 與 **Google Apps Script (GAS)** 的全方位加密憑證管理工具。它採用 **AES-256 高強度加密技術**，確保您的 API Key 與 Bot Token 即使存儲在雲端也能擁有極致的安全性。

---

## ✨ 功能亮點

- **🔒 零知識證明架構**：主密碼永遠不離開您的瀏覽器，也不會存儲在任何伺服器。
- **🌫️ 高級毛玻璃 UI**：採用現代化 Glassmorphism 設計，具備流暢的動畫與深色模式。
- **🛡️ 安全驗證機制**：自訂主密碼驗證邏輯，確保只有您本人能進入保險箱。
- **🔍 即時搜尋過濾**：當憑證數量眾多時，可透過關鍵字快速定位所需金鑰。
- **📱 響應式設計**：完美支援手機與電腦瀏覽器操作。
- **⚡ 快速複製功能**：一鍵解密並複製到剪貼簿，並具備自動關閉的通知彈窗。

---

## 🛠️ 技術堆疊

- **Frontend**: HTML5, CSS3 (Blur effect), JavaScript (ES6+)
- **Security**: CryptoJS (AES-256)
- **Backend**: Google Apps Script (GAS)
- **Database**: Google Sheets API

---

## 🚀 快速開始

### 1. 準備資料庫 (Google Sheets)
1. 建立一個新的 Google 試算表。
2. 將第一列標題設為：`ID`, `Type`, `Name`, `Content`, `Date`。
3. 複製試算表網址中的 **ID** (位於 `/d/` 與 `/edit` 之間的字串)。

### 2. 部署後端 (GAS)
1. 在試算表中點擊 `擴充功能` > `Apps Script`。
2. 貼入專案提供的 `code.gs` 程式碼。
3. 修改 `SHEET_ID` 為您剛才複製的 ID。
4. 點擊 `部署` > `新部署作業`。
5. 類型選擇 `網頁應用程式`，並將「誰可以存取」設為 `所有人`。
6. **複製生成的 Web App URL**。

### 3. 設定前端 (GitHub Pages)
1. 將 `index.html` 上傳至您的 GitHub 儲存庫。
2. 修改 `index.html` 中的 `GAS_URL` 變數，貼入剛才得到的 Web App URL。
3. 開啟儲存庫的 `Settings` > `Pages`，選擇來源並儲存。

---

## 🛡️ 安全注意事項

1. **主密碼是唯一鑰匙**：如果您遺失了主密碼，存儲在雲端的資料將無法被還原。
2. **不要洩漏 URL**：雖然有密碼保護，但建議不要公開分享您的 Web App URL 或 Sheets ID。
3. **定期備份**：您可以隨時手動導出 Google Sheets 中的資料作為備份（雖然內容是加密的）。

---

## 📜 授權協議
本專案採 MIT 協議授權，歡迎自由修改與分享。
