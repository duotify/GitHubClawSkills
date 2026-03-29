# 🛠️ Agent Browser

> 讓小龍蝦幫你操作瀏覽器——打開網站、填表單、點按鈕、截圖、抓資料，全部自動搞定！

## ✨ 這個技能可以做什麼？

- 🌐 自動開啟網站並瀏覽頁面，就像有人幫你操作瀏覽器一樣
- 📝 自動填寫表單、輸入帳密、勾選選項並送出
- 🖱️ 點擊按鈕、切換選單、等待頁面載入完成
- 📸 擷取網頁截圖（局部或整頁），把畫面存下來
- 🔍 抓取頁面上的文字內容，例如商品名稱、價格、標題等

## 📦 安裝方式

在 Telegram 對話中輸入：

```
/skills
```

輸入後會顯示可安裝的技能列表，選擇此技能即可完成安裝。

## 💬 提示詞範例

以下是你可以直接複製貼上跟小龍蝦說的話：

```text
幫我打開 https://example.com，登入後截一張全頁圖。
請到這個網站填完表單，提交後告訴我結果頁面顯示什麼。
開啟後台 dashboard，檢查是否有出現 Welcome 訊息。
進入產品列表頁，擷取第一個商品名稱與價格。
幫我自動操作這個 Web App，重現新增資料的流程。
```

## 📝 輸出範例

小龍蝦會根據你的指令回傳不同結果，例如：

- **截圖**：一張網頁畫面的圖片（PNG 格式）
- **文字擷取**：從頁面上抓到的內容，像是：
  ```
  商品名稱：龍蝦堡限定公仔
  價格：NT$350
  ```
- **操作結果**：告訴你表單是否送出成功、頁面跳轉到哪裡

## ⚠️ 注意事項

- 🖥️ 系統需要有安裝 **Chrome 或 Chromium** 瀏覽器才能運作
- 🔄 小龍蝦操作網頁時使用「**開啟 → 快照 → 互動 → 重新快照**」的流程。每次頁面變化後，舊的元素參照（如 `@e1`）會失效，需要重新快照
- 🔐 如果有登入狀態檔案（如 `auth.json`），請不要上傳到公開的地方
- 🏁 操作完畢後，小龍蝦會自動關閉瀏覽器

## 🔗 延伸閱讀

- 技術細節請參考 [SKILL.md](SKILL.md)
- 指令完整列表：[references/commands.md](references/commands.md)
- 登入驗證流程：[references/authentication.md](references/authentication.md)
- 元素參照與快照規則：[references/snapshot-refs.md](references/snapshot-refs.md)
- Session 管理：[references/session-management.md](references/session-management.md)
- 現成自動化範本：[templates/](templates/) 目錄
