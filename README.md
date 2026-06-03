# 第二次世界大戰人生模擬器

一個沉浸式、歷史準確的二戰人生模擬遊戲。

## 🎮 快速開始

### 方式1：直接雙擊（最簡單）

1. 下載 `wwii-simulator.html` 和 `logo.png`
1. 將兩個檔案放在**同一資料夾**
1. **雙擊 `wwii-simulator.html` 開啟**
1. 開始遊戲

✅ 無需安裝、無需網絡、完全離線  
✅ 進度自動存在你的電腦  
✅ Logo 自動載入到瀏覽器標籤和 iPhone 主畫面

**Logo 說明**：見 <LOGO-GUIDE.md>

-----

## 💾 進度管理

### 自動存檔

- 每完成一個回合，進度自動儲存在你的瀏覽器
- 關閉遊戲後，下次開啟時自動恢復進度

### 手動匯出進度

1. 遊戲中點擊「📥 下載進度」
1. 自動下載 JSON 檔案（例如：林愉朗_45回合.json）
1. 保存檔案作為備份

### 分享進度給朋友

#### 方式1：複製分享代碼（推薦）

1. 遊戲中點擊「📋 複製分享代碼」
1. 分享代碼（長字符）給朋友
1. 朋友貼上代碼，點擊「📌 貼上分享代碼」
1. ✅ 朋友即可繼續你的故事

#### 方式2：上傳 JSON 檔案

1. 先下載你的進度（見上）
1. 用 WeChat / Email 傳 JSON 檔案給朋友
1. 朋友開啟模擬器，點擊「📤 上傳進度」
1. 選擇你的 JSON 檔案
1. ✅ 朋友即可繼續你的故事

-----

## 🌐 在線分享版本（GitHub Pages）

如果你有 GitHub 帳號，可以將模擬器上傳到 GitHub Pages，朋友只需一個連結即可遊玩。

### 設置步驟

#### 1. 建立 GitHub 倉庫

```bash
# 初始化本地 git 倉庫
git init

# 建立 index.html（將 wwii-simulator.html 改名）
mv wwii-simulator.html index.html

# 新增檔案
git add index.html README.md LOGO-GUIDE.md

# 如果有 logo.png，也加入
# git add logo.png

# 提交
git commit -m "Initial commit: WWII Life Simulator"
```

#### 2. 推送到 GitHub

```bash
# 設置遠程倉庫（替換 YOUR_USERNAME）
git remote add origin https://github.com/YOUR_USERNAME/wwii-simulator.git

# 推送到主分支
git branch -M main
git push -u origin main
```

#### 3. 上傳 Logo（可選但推薦）

```bash
# 將 logo.png 複製到倉庫目錄
cp logo.png /path/to/wwii-simulator/

# Push 到 GitHub
git add logo.png
git commit -m "🎖️ Add logo"
git push
```

#### 3. 啟用 GitHub Pages

1. 在 GitHub 上開啟倉庫
1. Settings → Pages
1. 選擇 Branch: `main` → 儲存
1. 等待 1–2 分鐘
1. ✅ 你的遊戲可在以下地址遊玩：

```
https://YOUR_USERNAME.github.io/wwii-simulator/
```

### 分享給朋友

只需分享這個連結：

```
https://YOUR_USERNAME.github.io/wwii-simulator/
```

朋友開啟連結即可遊玩。進度仍然存在他們的瀏覽器（各自獨立）。

-----

## 🔄 更新模擬器

如果你修改了 `index.html` 並想推送新版本：

```bash
git add index.html
git commit -m "Update: Add new features"
git push
```

朋友重新整理頁面，自動使用最新版本。

-----

## 🎯 遊戲特色

### DM 系統

- 世界獨立於玩家運行
- 歷史事件按真實時間線發生
- NPC 自主行動、升遷、死亡
- 每個選擇都有代價

### 數值系統

- 健康、士氣、資金、魅力
- 戰鬥疲勞、創傷壓力
- 軍中聲望、政治風險
- 動態影響遊戲結果

### 故事沉浸感

- 300+ 字的劇情描述
- NPC 互動對話
- 歷史線索與證據
- 多選項決策樹

-----

## 📱 兼容性

✅ Windows / Mac / Linux（雙擊 .html）  
✅ 所有現代瀏覽器（Chrome, Firefox, Safari, Edge）  
✅ 手機（用瀏覽器開啟）

-----

## 🚀 技術細節

- **純 HTML/CSS/JavaScript**（無外部依賴）
- **localStorage 本機存檔**（隱私安全）
- **Claude API 驅動**（每回合動態生成）
- **單檔案部署**（易於分享）

-----

## ⚠️ 注意事項

### API 密鑰

模擬器使用 Claude API 生成劇情。為了正常運作，需要有效的 API 密鑰。

如果出現 API 錯誤，請檢查：

1. 網絡連接
1. Claude API 額度是否充足
1. 瀏覽器控制台是否有錯誤信息

### 隱私

- 進度完全存在你的本機或朋友的本機
- 分享代碼和 JSON 檔案包含完整遊戲狀態
- 不涉及第三方服務器

-----

## 📞 問題排除

|問題           |解決                                  |
|-------------|------------------------------------|
|無法開啟 .html 檔案|用瀏覽器拖進去或右鍵「用程式開啟」                   |
|進度遺失         |檢查瀏覽器是否清除了 localStorage；可用 JSON 檔案恢復|
|API 錯誤       |檢查網絡；確認 Claude 帳號有額度                |
|分享代碼無效       |確保完整複製代碼；避免換行或額外空格                  |

-----

## 🎓 學習資源

如果你想修改或擴展模擬器，可參考：

- **HTML/CSS**：修改樣式和排版
- **JavaScript**：修改遊戲邏輯、數值系統
- **Claude API**：修改 DM 提示詞（system prompt）

-----

## 📝 版本歷史

**v1.0**（2026年6月）

- ✅ 完整角色建立系統
- ✅ localStorage 自動存檔
- ✅ 進度匯出/匯入（JSON + 分享代碼）
- ✅ 實時 Claude API 驅動劇情
- ✅ 8 項動態數值系統
- ✅ NPC 互動與線索系統

-----

## 🙋 回饋與建議

如果有任何問題或建議，可以：

1. 檢查 HTML 原始碼（F12 開發者工具）
1. 修改 DM 提示詞以改變故事風格
1. 調整數值系統以改變難度

祝遊戲愉快！⚔️