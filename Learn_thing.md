# 🏥 自製長照 AI ALYA：FHIR 作品說明書
> **隊伍名稱**：安平鎮工所
> **主題領域**：人工智慧、長期照護、IOT 數值讀取與採集

---

## 📝 基本資訊
* **作品名稱**：自製長照 AI ALYA 
* **核心 FHIR Resources**：Personal Health Record (PHR)

---

## 📖 專案摘要 (Abstract)
我們運用 **Google AI Gemini** 教導製作以聊天為主的自製型 AI (Alya) [cite: 9][cite_start]。核心採用 **LLaMA-3-8B** 大型語言模型，並透過 Gemini 逐步引導關於 AI 的定義與專案修改方向，旨在填補目前長照資源端缺少的輔助型 AI 聊天助理 [cite: 9][cite_start]。在製作過程中，透過微調與核心指令調整，使其達成專案目標 [cite: 9]。

---

## 🎓 FHIR 課程紀錄

### (一) FHIR 是什麼：
* **現代化互通性**：使用網際網路常見的 **RESTful API**，讓醫療資料交換跟上行動化潮流。
* **數據模組化 (Resources)**：將病歷資料拆分為 **135 個大類**（如病患、醫令、檢驗報告），如同組裝積木般靈活且一致。
* **延伸性與靈活性**：提供 **Extension 欄位**，可自定義欄位以滿足特定醫療需求。
* **輕量化格式**：支援 **JSON** 和 **XML** 格式，傳輸效率高。
* **跨領域應用**：適用於院內系統整合（HIS、LIS、PACS）、跨院資料共享、遠距醫療及健康管理。

### (二) 專案所運用的 FHIR 是什麼 (PHR)：
**PHR（個人健康紀錄）** 是由病患自主持有與管理的健康數據，包含病史、用藥及自測生理數據，強調個人化與全人照護。**FHIR** 則是將這些分散資料標準化的技術規範。
* **定義**：指病患本身持有、維護與管理的健康與醫療記錄，不同於醫院持有的 **EMR（電子病歷）**。
* **內容**：包括就醫記錄、檢驗報告、藥物資訊、運動習慣、飲食喜好、居家檢測數據（如血壓、血糖）等。
* **目的**：提供病患全面的健康歷史，協助醫生進行更精準的照護。

---

## 🛠️ 資源介紹 (Tools & Resources)

| 名稱 | 說明 |
| :--- | :--- |
| **NVIDIA RTX™ 5000 Ada** | [cite_start]提供大型語言模型運算算力 [cite: 11] |
| **凱比機器人** | [cite_start]與自製 AI 進行功能對比 [cite: 11] |
| **Visual Studio Code / Antigravity** | [cite_start]程式撰寫平台 [cite: 11] |
| **Python** | [cite_start]主要開發程式語言 [cite: 11] |
| **LLaMA-3-8B** | [cite_start]核心大型語言模型 [cite: 11] |
| **Draw.io** | [cite_start]製作流程圖工具 [cite: 11] |
| **HuggingFace** | [cite_start]模型來源平台 [cite: 11] |
| **CodeLab** | [cite_start]凱比機器人程式撰寫網頁 [cite: 11] |
| **Adafruit** | [cite_start]物聯網 (IOT) 數據平台 [cite: 11] |

---

## 🧠 作品核心介紹

### 1. 自製型 AI 聊天系統
[cite_start]以 **LLaMA-3** 為大腦，分為三大模塊 [cite: 14]：
* [cite_start]**生成式對話**：透過 **LLaMA-Factory** 進行人格微調，Alya 能根據輸入生成具備「性格特質」（如：俄系傲嬌）的非固定式回覆 [cite: 15]。
* [cite_start]**主動社交機制**：後端監控線程會在使用者長時間未互動時，主動發起關懷對話，模擬真人社交行為以降低孤獨感 [cite: 16]。
* [cite_start]**多模態情感聯動**：結合 AI 判讀結果與情感表現 [cite: 14]。

### 2. IOT 數值採集
[cite_start]運用 **Adafruit** 金鑰連結 IOT 設備，實現生理數值的自動存入與讀取功能 [cite: 17]。

---

## 🎭 劇本模擬 (Scenario)

* [cite_start]**情境敘述**：一位患有糖尿病、高血壓的高齡患者，因子女工作繁忙無暇照顧，需要系統協助記錄數值並紓解孤單 [cite: 19, 21, 22]。
* **情境目標**：
    * [cite_start]避免因健忘而遺漏身體檢測 [cite: 23]。
    * [cite_start]提供日常身體資料供專業醫生檢查時參考 [cite: 24]。
* **需求分析**：
    * [cite_start]似人類口吻聊天並記錄狀態 [cite: 26, 27]。
    * [cite_start]發現異常時發出警訊並定期製作報告 [cite: 28, 29]。
* **工作流程**：
    1. [cite_start]收到 APP 訊息進行每日生理數值採集 [cite: 31]。
    2. [cite_start]採集完畢向 AI 回報 [cite: 32]。
    3. [cite_start]AI 針對數值給予關懷與衛教建議 [cite: 33]。
* [cite_start]**特殊劇情**：連動智能手錶進行隨時監測，異常時發出警訊 [cite: 34]。

---

## 👥 使用角色
* [cite_start]**長者** [cite: 35]
* [cite_start]**需要隨時觀測數值的病人** [cite: 35]
* [cite_start]**獨居老人** [cite: 35]

---

## 📑 主要 FHIR Resources 定義
* [cite_start]**Patient**: 使用者的基本資料（姓名、生日、性別、聯絡方式） [cite: 37]。
* [cite_start]**Observation**: 生理量測數值（心率、血壓、體溫等數據） [cite: 38]。
* [cite_start]**Device**: 醫療物聯網硬體資訊（Arduino 或感測器描述） [cite: 39]。
* [cite_start]**Communication**: Alya 與使用者之間的關懷對話與衛教紀錄 [cite: 40]。

---
© 2026 安平鎮工所 專案團隊
