# 🚀 GitHub 部署步驟 / GitHub Deployment Guide

## 📋 前置準備 / Prerequisites

1. **GitHub 帳號** - 如果沒有，請到 https://github.com 註冊
2. **準備好的圖片** - 5 張菜品照片（見 images/README.md）

## 🎯 部署步驟 / Deployment Steps

### 步驟 1: 建立 Repository

1. 登入 GitHub
2. 點擊右上角的 "+" > "New repository"
3. 填寫資料：
   - **Repository name**: `sister-menu` 或其他名稱
   - **Description**: 姊妹小吃電子菜單
   - **Public**: 選擇 Public（才能使用 GitHub Pages）
   - ✅ 勾選 "Add a README file"
4. 點擊 "Create repository"

### 步驟 2: 上傳檔案

#### 方法 A: 透過網頁介面（簡單）

1. 在 repository 頁面，點擊 "Add file" > "Upload files"
2. 拖曳以下檔案到上傳區：
   ```
   index.html
   README.md
   .gitignore
   ```
3. 創建 `images` 資料夾：
   - 點擊 "Create new file"
   - 輸入 `images/README.md`
   - 複製 `images/README.md` 的內容
   - 點擊 "Commit new file"
4. 上傳圖片到 `images` 資料夾：
   - 進入 `images` 資料夾
   - 點擊 "Add file" > "Upload files"
   - 上傳 `logo.png` 和 4 張菜品照片
   - 確認檔名正確：
     - logo.png
     - guzao-noodles.jpg
     - guzao-vermicelli.jpg
     - chicken-leg-soup.jpg
     - soup-dumplings.jpg

#### 方法 B: 透過 Git 指令（進階）

```bash
# 1. Clone repository
git clone https://github.com/你的帳號/sister-menu.git
cd sister-menu

# 2. 複製所有檔案到這個資料夾
# （包含 index.html, README.md, .gitignore 和 images 資料夾）

# 3. 加入所有檔案
git add .

# 4. 提交變更
git commit -m "初始版本：姊妹小吃電子菜單"

# 5. 推送到 GitHub
git push origin main
```

### 步驟 3: 啟用 GitHub Pages

1. 在 repository 頁面，點擊 "Settings"
2. 在左側選單找到 "Pages"
3. 在 "Build and deployment" 區域：
   - **Source**: 選擇 "Deploy from a branch"
   - **Branch**: 選擇 "main"，資料夾選擇 "/ (root)"
4. 點擊 "Save"
5. 等待 1-2 分鐘，頁面會顯示網址
6. 點擊網址即可查看你的電子菜單！

### 步驟 4: 取得網址

網址格式會是：
```
https://你的帳號.github.io/sister-menu/
```

例如：
```
https://johnsmith.github.io/sister-menu/
```

## ✅ 檢查清單 / Checklist

部署完成後請確認：

- [ ] 網站可以正常開啟
- [ ] Logo 正確顯示
- [ ] 4 張菜品圖片都正確顯示
- [ ] 中英文內容正確
- [ ] 在手機上測試點餐流程
- [ ] 測試 LINE 傳送訂單功能
- [ ] 價格、菜名都正確

## 📱 測試方式 / Testing

1. **桌面測試**：直接在電腦瀏覽器開啟
2. **手機測試**：
   - 方法 1: 用手機瀏覽器開啟網址
   - 方法 2: 製作 QR Code 讓顧客掃描
3. **LINE 測試**：
   - 選擇菜品加入購物車
   - 點擊「傳送訂單到 LINE」
   - 確認能正確開啟 LINE 並帶入訂單內容

## 🔄 更新內容 / Update Content

如需修改菜單內容：

1. 編輯 `index.html` 檔案
2. 上傳到 GitHub（使用網頁或 Git 指令）
3. 等待 1-2 分鐘自動部署
4. 重新整理網頁查看更新

## 🎨 自訂網址（選用）

如果你有自己的網域名稱：

1. 在 DNS 設定中加入 CNAME 記錄：
   ```
   www  CNAME  你的帳號.github.io
   ```
2. 在 GitHub Pages 設定中輸入你的網域
3. 等待 DNS 生效（可能需要 24 小時）

## 📊 追蹤使用情況（選用）

可以加入 Google Analytics 來追蹤：
- 有多少人瀏覽菜單
- 哪些菜品最受歡迎
- 瀏覽時段分布

## 🆘 常見問題 / FAQ

### Q: 圖片無法顯示？
A: 
1. 檢查檔名是否完全一致
2. 確認圖片在 `images/` 資料夾內
3. 清除瀏覽器快取

### Q: GitHub Pages 網址打不開？
A: 
1. 確認已在 Settings > Pages 啟用
2. 等待 1-2 分鐘讓系統部署
3. 檢查 Actions 標籤確認部署狀態

### Q: 修改後沒有更新？
A: 
1. 確認檔案已成功上傳
2. 清除瀏覽器快取（Ctrl+F5）
3. 等待幾分鐘讓系統重新部署

### Q: LINE 傳送功能無法使用？
A: 
1. 確認 LINE 官方帳號 ID 正確
2. 檢查手機是否已安裝 LINE
3. 測試是否有網路連線

## 📞 需要協助？ / Need Help?

如遇到任何問題，歡迎：
1. 查看 GitHub 官方文件：https://docs.github.com/pages
2. 搜尋相關教學影片
3. 透過 LINE @sister666 聯絡我們

---

**祝你部署順利！🎉**
