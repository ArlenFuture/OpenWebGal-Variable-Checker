# OpenWebGal 變數檢查工具

這個工具專為 **OpenWebGal** 專案開發，旨在幫助開發者檢查跨多個 `.txt` 文件中，變數是否有未宣告使用的問題，以及大小寫不一致的問題。工具會從 `start.txt` 開始，並按照 `changeScene` 語法遍歷場景文件，確保所有變數都正確處理。

## 功能特點
- **跨檔案變數檢查**：檢查多個 `.txt` 文件中是否有未宣告的變數。
- **大小寫敏感檢測**：識別變數宣告與使用時的大小寫不一致問題。
- **場景文件遍歷**：從 `start.txt` 開始，根據 `changeScene` 語法檢查所有相關的場景文件。

## 使用方法
1. **上傳文件**：你可以一次上傳多個 `.txt` 文件，包括 `start.txt` 和其他場景文件。
2. **執行檢查**：工具會自動檢查變數的使用情況，並顯示結果。
3. **檢查結果**：結果會指出未宣告的變數或大小寫問題，並標示文件名稱與行號。

### 語法範例
以下是工具會解析的 OpenWebGal 語法範例：

```plaintext
setVar:Child=false
setVar:ZYknowXX=false
changeScene:Chapter-1.txt
jumpLabel:label_60 -when=ZYknowXX==true
```

## 專案設定

如果想要在本地端運行此工具：

1. 下載 `index.html`。
2. 並開於瀏覽器中。

## 文件結構

```plaintext
.
├── index.html        # 網頁主頁面，包含變數檢查工具
└── examples/
    ├── start.txt     # 範例的起始文件
    └── Chapter-1.txt # 範例的場景文件
```

## 貢獻

如果你想要貢獻此專案，歡迎提交 Pull Request 或回報 Issue。我們很歡迎任何功能改進、新增功能或 Bug 修復的貢獻！

## 授權條款

此專案使用 MIT 授權條款 - 詳見 [LICENSE](LICENSE) 文件。
