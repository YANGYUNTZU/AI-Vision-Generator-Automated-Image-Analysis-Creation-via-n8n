# 🤖 n8n AI Image Generator: Chat-to-DALL·E Workflow

這個專案展示了如何利用 **n8n** 構建一個全自動化的 AI 影像生成工作流。使用者只需透過對話介面輸入指令，系統即可自動調用 OpenAI DALL·E 3 模型產出高品質圖片。

## 🌟 核心功能

* **對話式觸發 (Chat Interface)**：整合 n8n 的 `When chat message received` 觸發節點，提供直觀的互動體驗。
* **動態提示詞技術**：系統自動擷取對話內容 `{{ $json.chatInput }}` 並動態注入 AI 模型中，實現零延遲響應。
* **高品質影像生成**：使用 OpenAI DALL·E 3 旗艦模型，支援精準的場景構圖與文字理解。
* **自動化二進位處理**：產出的影像會自動轉換為 `.png` 格式，方便後續的存儲或分享。

## 🛠 技術堆棧

* **工作流引擎**：n8n
* **AI 模型**：OpenAI DALL·E 3
* **輸入介面**：n8n Chat (Beta)

## 📋 工作流邏輯說明

1.  **監聽階段 (Input)**：
    * 節點：`When chat message received`。
    * 功能：接收使用者輸入的文字指令（例如：「請幫我生成柯基狗奔跑在草原的圖片」）。
2.  **生成階段 (Processing)**：
    * 節點：`Generate an image` (OpenAI)。
    * 配置：串接 `OpenAI account` 憑證，並將 `Resource` 設為 Image，`Operation` 設為 Generate。
3.  **成果展示 (Output)**：
    * 結果：產生 binary 圖片檔案（如 1.48 MB 的 png 文件）。

## 🚀 快速上手

1.  **環境準備**：確保已安裝 n8n 並擁有 OpenAI API Key。
2.  **導入 JSON**：將專案中的 `.json` 工作流檔案匯入 n8n。
3.  **配置憑證**：在 OpenAI 節點中選擇您的 `OpenAI account`。
4.  **開始執行**：點擊 **"Open chat"** 測試您的第一張 AI 圖片。

## 📸 實測截圖

![n8n Workflow Demo]
*圖：系統成功根據提示詞生成柯基犬在草原奔跑的影像。*

---
Made with ❤️ by [Your Name]
