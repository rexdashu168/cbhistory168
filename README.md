# 可轉債查詢系統 - 完全自動化

## 🎯 特色

✅ **完全自動化** - 只需上傳Excel，系統自動更新
✅ **秒開網頁** - 無需等待載入
✅ **即時更新** - 資料變更30秒內生效

---

## 📁 檔案結構

```
cbhistory168/
├── .github/
│   └── workflows/
│       └── update-data.yml    # 自動化腳本（不用動）
├── index.html                 # 網頁主程式（不用動）
├── cb_issue.xlsx             # Excel資料檔（每月更新這個）
├── cb_data.json              # JSON資料（自動生成，不用管）
└── README.md                 # 說明文件
```

---

## 🚀 使用方式

### 初次設定（只需一次）

1. **上傳所有檔案到GitHub**
   - 到 https://github.com/rexdashu168/cbhistory168
   - 上傳所有檔案

2. **啟用GitHub Actions**
   - Settings → Actions → General
   - Workflow permissions 選擇 "Read and write permissions"
   - 點擊 Save

3. **完成！**
   - 訪問 https://rexdashu168.github.io/cbhistory168/

---

### 每月更新（超簡單）

1. **準備Excel檔案**
   - 檔名：`cb_issue.xlsx`
   - 工作表名稱：`allcbissue`
   - 確認欄位完整

2. **上傳到GitHub**
   - 打開 https://github.com/rexdashu168/cbhistory168
   - 點擊 `Add file` → `Upload files`
   - 選擇 `cb_issue.xlsx`
   - 勾選 "Replace file"
   - 點擊 `Commit changes`

3. **等待30秒**
   - GitHub自動轉換資料
   - 網頁自動更新

4. **完成！** ✅

---

## 📊 必要欄位

Excel必須包含以下欄位：

- CB代碼
- CB名稱
- 股票代碼
- 發行規模
- 有無擔保
- 發行年期
- 轉換價格
- 掛牌日期
- 下市日期
- 掛牌最高
- 掛牌最低
- 賣回日期1、賣回日期2
- 賣回價格1、賣回價格2
- 賣回殖利率1、賣回殖利率2
- 承銷券商
- 產業分類
- 承銷方式
- 股本規模

---

## 🔍 檢查自動化狀態

1. 到 GitHub repo
2. 點擊 `Actions` 標籤
3. 查看最新的 workflow 執行狀況
4. ✅ 綠色勾勾 = 成功
5. ❌ 紅色叉叉 = 失敗（檢查錯誤訊息）

---

## ❓ 常見問題

**Q: 上傳後沒自動更新？**
A: 
1. 檢查 Settings → Actions 是否已啟用
2. 確認檔名是 `cb_issue.xlsx`
3. 查看 Actions 標籤確認執行狀態

**Q: 網頁顯示舊資料？**
A: 
1. 清除瀏覽器快取（Ctrl+F5）
2. 等待1-2分鐘讓GitHub Pages更新

**Q: 想手動觸發更新？**
A:
1. 到 Actions 標籤
2. 選擇 "自動更新可轉債資料"
3. 點擊 "Run workflow"

---

## 🎉 就是這麼簡單！

上傳Excel → 自動更新 → 完成！
