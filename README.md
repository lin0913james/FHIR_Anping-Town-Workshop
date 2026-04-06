# [cite_start]🏥 自製長照 AI ALYA [cite: 4]
> [cite_start]**隊伍名稱**：安平鎮工所 [cite: 3]  
> [cite_start]**主題領域**：人工智慧、長期照護、IOT [cite: 5]

---

## [cite_start]🌟 專案摘要 (Abstract) [cite: 8]
[cite_start]本專案透過 **Google AI Gemini** 的指導，開發出一款以聊天為核心的自製型 AI 助手 —— **Alya** [cite: 9][cite_start]。我們採用 **LLaMA-3-8B** 作為大型語言模型，並針對目前長照資源短缺的現況，將其微調為具備專業輔助能力的聊天助理 [cite: 9][cite_start]。Alya 能透過微調與核心指令，達成專案設定的長照護理目標 [cite: 9]。

## [cite_start]👥 使用者角色 (User Personas) [cite: 6, 35]
本系統主要服務對象包含：
* [cite_start]**獨居老人**：需要情感陪伴以緩解孤獨感 [cite: 6, 35]。
* [cite_start]**慢性病患者**：如糖尿病、高血壓患者，需要定時監測生理數值 [cite: 6, 19]。
* [cite_start]**身心疾病患者**：需要溫暖的關懷與定時的心理支持 [cite: 6]。

---

## [cite_start]🛠️ 技術資源與工具 [cite: 10, 11]

| 名稱 | 說明 |
| :--- | :--- |
| **NVIDIA RTX™ 5000 Ada** | [cite_start]提供大型語言模型運算算力 [cite: 11] |
| **LLaMA-3-8B** | [cite_start]系統核心大型語言模型 [cite: 11] |
| **Adafruit** | [cite_start]物聯網 (IOT) 數據存取與讀取平台 [cite: 11, 17] |
| **Python / VS Code** | [cite_start]程式開發語言與撰寫平台 [cite: 11] |
| **凱比機器人** | [cite_start]作為與自製 AI 對比之硬體平台 [cite: 11] |
| **HuggingFace** | [cite_start]模型來源庫 [cite: 11] |

---

## [cite_start]🧠 核心技術說明 (Technical Details) [cite: 12]

### [cite_start]1. 生成式對話與人格微調 [cite: 15]
[cite_start]透過 **LLaMA-Factory** 進行人格微調，讓 Alya 具備特定性格（如：俄系傲嬌），能根據使用者語境生成非固定式的靈活回覆 [cite: 15]。

### [cite_start]2. 主動社交機制 [cite: 16]
[cite_start]後端架設時間序列監控線程，當偵測到使用者長時間未互動時，系統會主動發起關懷對話，模擬人類社交行為以降低使用者孤獨感 [cite: 16]。

### [cite_start]3. IOT 數值採集 [cite: 17]
[cite_start]運用 **Adafruit 金鑰** 實現 AI 與 IOT 設備的連結，達成生理數據的即時存入與讀取 [cite: 17]。

---

## [cite_start]📑 FHIR 資源規劃 (FHIR Resources) [cite: 36]
[cite_start]本專案以 **PHR (Personal Health Record)** 為核心架構 [cite: 7, 36]，實作以下資源：

* [cite_start]**Patient**: 使用者的基本資料，包含姓名、生日、性別與聯絡方式 [cite: 37]。
* [cite_start]**Observation**: 紀錄由 IoT 設備採集的心率、血壓、體溫等生理量測資料 [cite: 38]。
* [cite_start]**Device**: 描述醫療物聯網硬體資訊（如 Arduino 或感測器模組） [cite: 39]。
* [cite_start]**Communication**: 紀錄 Alya 與使用者間的衛教內容與關懷對話 [cite: 40]。

---

## [cite_start]🔄 工作流程 (Workflow) [cite: 30]
1. [cite_start]**數值採集**：系統定時透過 APP 發起身體數值採集需求 [cite: 31]。
2. [cite_start]**數據回報**：採集完畢後將數值回傳至 AI 系統 [cite: 32]。
3. [cite_start]**AI 關懷**：AI 針對數值進行分析，並給予使用者相應的建議與關懷 [cite: 33]。
4. [cite_start]**異常監測**：若連動之智能手錶偵測到異常，系統會立即發出警訊 [cite: 34]。

---

## [cite_start]🎭 情境劇本範例 [cite: 18, 19]
* [cite_start]**情境**：一位患有糖尿病與高血壓的長者，因子女繁忙而獨自在家 [cite: 19, 21]。
* [cite_start]**目標**：紓解孤單、提醒定時檢測、並在就醫時提供詳盡的日常紀錄 [cite: 22, 23, 24]。
* [cite_start]**需求分析**：AI 需以類人語調聊天，並在發現異常時發出警訊 [cite: 26, 28]。

---
© 2026 安平鎮工所 專案小組
