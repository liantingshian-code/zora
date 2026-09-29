# 🌟 小孩每日任務點數表

一個純前端、免安裝的兒童每日任務點數表，讓小孩完成每日任務賺取點數，集滿點數即可兌換獎勵。

## ✨ 功能特色

- 📋 **每日任務清單**：點擊即可打勾／取消，自動計算今日點數
- ⭐ **累積點數**：跨日累積，集點換獎勵
- 📊 **進度條**：即時顯示今日任務完成進度
- 🎉 **完成慶祝**：全部完成時顯示祝賀動畫
- ⚙️ **家長專區**：
  - 🎁 獎勵兌換（可依點數兌換看電視、玩具、故事書等）
  - 🔄 重設今日任務
  - 🗑️ 重設全部（清除所有點數）
- 📱 **手機友善**：響應式設計，支援手機瀏覽器
- 💾 **資料保存**：使用瀏覽器 localStorage 儲存，跨日自動重置任務

## 🚀 使用方式

### 本機使用

直接用瀏覽器開啟 `index.html` 即可，不需任何伺服器或安裝程序。

### 部署到 GitHub Pages

1. 在 GitHub 建立一個新的 Repository
2. 將本專案推送上傳：

   ```bash
   git remote add origin https://github.com/<你的帳號>/<repository名稱>.git
   git branch -M main
   git push -u origin main
   ```

3. 到 GitHub 專案頁面 → **Settings** → **Pages**
4. Source 選擇 `Deploy from a branch`，Branch 選擇 `main` / `/(root)`，按 Save
5. 稍後即可透過 `https://<你的帳號>.github.io/<repository名稱>/` 存取

## 🛠️ 技術

- 純 HTML / CSS / JavaScript，無外部依賴
- 資料儲存：瀏覽器 localStorage

## 📝 自訂任務與獎勵

編輯 `index.html` 中的兩個陣列即可調整內容：

```js
// 每日任務（points 為完成可獲得的點數）
const TASKS = [
  { emoji: "📔", text: "拿聯絡本出來給家長簽名", points: 1 },
  ...
];

// 獎勵兌換（cost 為兌換所需點數）
const REWARDS = [
  { emoji: "📺", text: "看電視 2 次（每次 40 分鐘）", cost: 25 },
  ...
];
```

## ⚠️ 注意事項

- 資料儲存在瀏覽器 localStorage 中，清除瀏覽器資料或更換裝置／瀏覽器後點數會歸零
- 同一裝置使用同一瀏覽器開啟即可保留紀錄
