# 課程前測問卷系統

純前端問卷調查系統，無需後端伺服器，所有資料儲存在瀏覽器 LocalStorage 中。

## 📁 專案結構

```
├── index.html      # 問卷填寫頁面
├── admin.html      # 後台管理與統計頁面
└── README.md       # 本說明文件
```

## 🚀 部署到 GitHub Pages

### 步驟 1：建立 GitHub 帳號與 Repository

1. 前往 [GitHub](https://github.com/) 註冊帳號（若還沒有帳號）
2. 點擊右上角 **+** → **New repository**
3. 填寫 Repository 名稱，例如：`survey-system`
4. 選擇 **Public**（公開）
5. 勾選 **Add a README file**（可選）
6. 點擊 **Create repository**

### 步驟 2：上傳檔案到 Repository

#### 方法 A：使用網頁上傳

1. 在你的 Repository 頁面，點擊 **Add file** → **Upload files**
2. 將以下檔案拖曳上傳：
   - `index.html`
   - `admin.html`
3. 填寫 Commit message，例如：`上傳問卷系統檔案`
4. 點擊 **Commit changes**

#### 方法 B：使用 Git 命令列

```bash
# 複製你的 Repository 到本地端
git clone https://github.com/你的帳號/你的repo名稱.git
cd 你的repo名稱

# 將檔案複製到資料夾中
# 複製 index.html 和 admin.html 到此資料夾

# 新增檔案到 Git
git add index.html admin.html

# 提交變更
git commit -m "上傳問卷系統檔案"

# 推送到 GitHub
git push origin main
```

### 步驟 3：啟用 GitHub Pages

1. 前往你的 Repository 頁面
2. 點擊上方的 **Settings**（設定）
3. 左側選單找到 **Pages**
4. 在 **Build and deployment** → **Source** 選擇 **Deploy from a branch**
5. 在 **Branch** 選擇 `main`（或 `master`）分支，資料夾選擇 `/ (root)`
6. 點擊 **Save**
7. 等待約 1-2 分鐘，重新整理頁面即可看到你的網站網址

網址格式：`https://你的帳號.github.io/你的repo名稱/`

## 📋 使用說明

### 學員填寫問卷

1. 將 GitHub Pages 網址分享給學員
2. 學員開啟 `index.html` 頁面（例如：`https://你的帳號.github.io/你的repo名稱/index.html`）
3. 填寫所有題目
4. 點擊 **提交問卷**，資料會自動儲存在瀏覽器 LocalStorage
5. 點擊 **下載 CSV** 可匯出所有填答結果

### 講師查看統計結果

1. 開啟後台管理頁面（例如：`https://你的帳號.github.io/你的repo名稱/admin.html`）
2. 輸入登入資訊：
   - **帳號：** `admin`
   - **密碼：** `123456`
3. 登入後可查看：
   - 總提交數
   - 各題目選項的統計數量（含長條圖視覺化）
   - 開放式問題的文字列表
4. 點擊 **下載 CSV** 匯出所有資料
5. 點擊 **重新載入** 可更新最新統計

## ⚠️ 重要注意事項

### LocalStorage 限制

- 資料儲存在**填寫者的瀏覽器 LocalStorage** 中
- **每位學員的資料都存在各自的瀏覽器裡**
- 講師要下載 CSV，必須在**同一台電腦、同一個瀏覽器**中查看所有學員提交的資料

### 建議使用方式

1. **集中填寫**：讓學員在同一台電腦（例如教室電腦）上依序填寫問卷
2. **講師下載**：講師在該電腦上開啟 `index.html`，點擊「下載 CSV」即可匯出所有資料
3. **查看統計**：在同一台電腦開啟 `admin.html`，登入後即可查看統計結果

### 若要支援跨裝置提交

如果需要學員從各自裝置填寫，並將資料統一收集，建議改用：
- Google 表單
- 帶有後端資料庫的問卷系統
- 其他雲端表單服務

## 🔧 技術細節

- **純前端**：HTML + CSS + JavaScript，無需安裝任何套件
- **資料儲存**：瀏覽器 LocalStorage
- **資料格式**：JSON（內部）/ CSV（匯出）
- **圖表顯示**：HTML 表格 + CSS 長條圖（不依賴外部套件）

## 📊 CSV 欄位說明

匯出的 CSV 包含以下欄位：

| 欄位 | 說明 |
|------|------|
| GitHub | GitHub 帳號註冊與使用熟悉度 |
| VSCode | VS Code 安裝與操作熟悉度 |
| Qwen | Qwen Code 擴充元件了解程度 |
| Pages | GitHub Pages 部署網站了解程度 |
| 期望學習內容 | 開放式問題：希望在課程中學到什麼 |
| 寫程式困難 | 開放式問題：目前寫程式最大的困難 |
| 提交時間 | 提交的時間戳記 |

## 🔒 安全性

- 後台預設帳號：`admin`
- 後台預設密碼：`123456`
- 如需修改，請編輯 `admin.html` 中的 `ADMIN_USERNAME` 和 `ADMIN_PASSWORD` 變數

## 📝 授權

本專案為教學用途，可自由使用與修改。
