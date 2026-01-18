# AI Image Master: n8n Workflow Studio 🤖🎨

這個專案包含了一套基於 **n8n** 構建的自動化工作流，整合了多種 AI 模型，實現「從文字到圖片生成」以及「影像視覺分析」的完整閉環。



## 🌟 核心功能

* **AI 圖片生成**：串接 OpenAI (DALL-E 3) 或 Midjourney API，根據輸入指令自動產出高品質影像。
* **AI 視覺分析**：利用 GPT-4o 或 Claude 3.5 Vision 分析上傳圖片，提取標籤、描述或進行 OCR 文字識別。
* **多平台整合**：支援透過 Telegram、Discord 或 Webhook 觸發任務並回傳結果。
* **自動化存儲**：將生成的圖片與分析結果自動同步至 Google Drive 或資料庫。

## 🛠 技術堆棧

* **Workflow Engine:** n8n
* **AI Models:** * Image Gen: OpenAI DALL-E 3 / Stable Diffusion
    * Analysis: OpenAI GPT-4o / Google Gemini Vision
* **Storage/Apps:** Google Drive, Telegram Bot, Airtable (依你的實際狀況修改)

## 🚀 快速上手

### 前置準備
1. 確保你已安裝並運行 [n8n](https://n8n.io/)。
2. 準備相關 AI 平台的 API Keys (OpenAI, Anthropic 等)。

### 安裝步驟
1. 下載本專案中的 `.json` 工作流文件。
2. 在 n8n 控制面板中點選 **"Import from File"**。
3. 在節點中配置你的 **Credentials** (憑證)。
4. 點擊 **"Execute Workflow"** 開始測試。

## 📂 專案結構
```text
.
├── workflows/
│   ├── image-generation-flow.json  # 圖片生成工作流
│   └── image-analysis-flow.json    # 影像分析工作流
├── assets/                         # 範例圖片與截圖
└── README.md
