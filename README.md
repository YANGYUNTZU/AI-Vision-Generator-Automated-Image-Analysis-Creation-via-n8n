# n8n AI 影像生成與圖片分析 🤖🎨

這個專案包含了一套基於 **n8n** ，整合AI 模型，實現「從文字到圖片生成」以及「影像視覺分析」的工作流程。



## 🌟 核心功能

* **AI 圖片生成**：串接 OpenAI (DALL-E 3) ，根據輸入指令自動產出高品質影像。
* **AI 視覺分析**：利用 GPT-4o-mini分析上傳圖片，提取標籤、描述或進行文字識別。

## 🛠 技術堆棧

* **Workflow Engine:** n8n
* **AI Models:** * Image Gen: OpenAI DALL-E 3 
* Analysis: OpenAI GPT-4o-mini 

## 🚀 快速上手

### 前置準備
1. 確保你已安裝並運行 [n8n]。
2. 準備相關 AI 平台的 API Keys (OpenAI, Anthropic 等)。

### 設定憑證 (Credentials)
* **OpenAI API**：用於驅動 AI Agent 進行推理。

## 📂 專案結構
```text
.
├── images/                        # 存放所有流程截圖與範例圖片
├── n8n AI Image Analysis/         # 影像分析工作流資料夾
│   ├── README.md                  # 影像分析功能說明
│   └── image-analysis-flow.json   # 影像分析工作流檔案
├── n8n AI Image Generator/        # 圖片生成工作流資料夾
│   ├── README.md                  # 圖片生成功能說明
│   └── image-generation-flow.json # 圖片生成工作流檔案
└── README.md                      # 專案總覽說明文件
