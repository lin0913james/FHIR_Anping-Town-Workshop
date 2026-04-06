# [cite_start]FHIR 作品說明書 [cite: 1, 2]

## 基本資訊
* [cite_start]**隊伍名稱**：安平鎮工所 [cite: 3]
* [cite_start]**作品名稱**：自製長照 AI ALYA [cite: 4]
* [cite_start]**主題領域**：人工智慧、長期照護、IOT [cite: 5]
* [cite_start]**使用者身分**：需要隨時有人幫忙紀錄身體數值者，並希望得到溫暖的關懷（如：獨居老人、病人、有身心疾病的患者） [cite: 6]
* [cite_start]**核心 FHIR Resources**：Personal Health Record (PHR) [cite: 7]

## [cite_start]摘要 [cite: 8]
[cite_start]我們運用到 Google AI Gemini 來教導我製作一個以聊天為主的自製型 AI (Alya) [cite: 9][cite_start]。我們是由 LLaMA-3-8B 為我們的大語言模型，並讓 Gemini 一步步教導我關於 AI 的定義與我們的 AI 專案要如何修改成最終的目標（可以填補目前長照資源端缺的輔助型 AI 聊天助理） [cite: 9][cite_start]。在製作過程中，我是以微調與給予核心指令進行調整成能夠達成專案目標的 AI [cite: 9]。

## [cite_start]資源介紹 [cite: 10]
| 名稱 | 說明 |
| :--- | :--- |
| NVIDIA RTX™ 5000 Ada Generation GPU | [cite_start]提供大型語言模型運算算力 [cite: 11] |
| 凱比機器人 | [cite_start]與自製 AI 進行對比 [cite: 11] |
| Visual Studio Code | [cite_start]撰寫程式平台 [cite: 11] |
| Antigravity | [cite_start]撰寫程式平台 [cite: 11] |
| Python | [cite_start]程式語言 [cite: 11] |
| LLaMA-3-8B | [cite_start]大型語言模型 [cite: 11] |
| Draw.io | [cite_start]製作流程圖 [cite: 11] |
| HuggingFace | [cite_start]模型來源 [cite: 11] |
| CodeLab | [cite_start]凱比機器人撰寫程式的網頁 [cite: 11] |
| Adafruit | [cite_start]物聯網 (IOT) 網頁 [cite: 11] |

## [cite_start]作品介紹 [cite: 12]

### [cite_start]二、自製型 AI 聊天 [cite: 13]
[cite_start]本研究運用 LLaMA-3 大型語言模型為 AI 的核心大腦 [cite: 14][cite_start]。本研究之自製 AI 可分為生成式對話、多模態情感聯動、主動社交機制三大部分 [cite: 14]。
* [cite_start]**生成式對話**：運用大型語言模型（LLM）之自然語言處理能力，透過 LLaMA-Factory 進行人格微調 [cite: 15][cite_start]。不同於預設劇本，自製 AI 能根據使用者的輸入即時生成具備「性格特質」（如：俄系傲嬌）的非固定式回覆，展現高靈活度的語境理解與對話持續性 [cite: 15]。
* [cite_start]**主動社交機制**：在系統後端架設基於時間序列的監控線程 [cite: 16][cite_start]。當偵測到使用者長時間未進行互動時，系統會突破「被動觸發」的限制，根據當前環境脈絡與歷史記憶，主動發起關懷對話 [cite: 16][cite_start]。此機制旨在模擬真實人類的社交行為，降低使用者的孤獨感 [cite: 16]。

### [cite_start]IOT 數值採集 [cite: 17]
[cite_start]我們運用 Adafruit 的金鑰讓我們的自製型 AI 能夠連結到 IOT 的數值以進行數值的存入與讀取 [cite: 17]。

## [cite_start]劇本模擬 [cite: 18]
* [cite_start]**情境敘述**：當前有一位患有糖尿病、高血壓的高齡患者想要使用本套系統來記錄數值 [cite: 19]。
* [cite_start]**情境目標** [cite: 20]：
    * [cite_start]長者的子女都時常因為工作繁忙而無暇照顧家中長者 [cite: 21]。
    * [cite_start]紓解長者孤單的情緒 [cite: 22]。
    * [cite_start]以免長者因為健忘而忘記定時自我檢測身體狀況 [cite: 23]。
    * [cite_start]在去與專業醫生檢查時可以提前拿出日常的身體資料 [cite: 24]。
* [cite_start]**需求分析** [cite: 25]：
    * [cite_start]聊天 AI，以似人類的口吻來聊天 [cite: 26]。
    * [cite_start]在與 AI 聊天的同時記錄長者狀態 [cite: 27]。
    * [cite_start]在發現長者出現異常時發出警訊 [cite: 28]。
    * [cite_start]定期製作出長者的身體數值報告 [cite: 29]。
* [cite_start]**工作流程** [cite: 30]：
    * [cite_start]收到來自 APP 的訊息並進行每日定期的身體數值採集 [cite: 31]。
    * [cite_start]在採集完數值後跟 AI 回報 [cite: 32]。
    * [cite_start]AI 針對數值進行關懷與建議 [cite: 33]。
* [cite_start]**特殊劇情**：在與使用者配戴的智能手錶進行連動再進行隨時監測，並在異常時發出警訊 [cite: 34]。

## [cite_start]使用角色 [cite: 35]
[cite_start]長者、與需要隨時觀測數值的病人、獨居老人 [cite: 35]。

## [cite_start]主要 FHIR Resources [cite: 36]
* [cite_start]**Patient**：使用者的基本資料（如：姓名、生日、性別、聯絡方式） [cite: 37]。
* [cite_start]**Observation**：生理量測數值（如：由 IoT 設備採集的心率、血壓、體溫等數據） [cite: 38]。
* [cite_start]**Device**：醫療物聯網硬體資訊（如：負責採集數據的 Arduino 或感測器設備描述） [cite: 39]。
* [cite_start]**Communication**：虛擬助手 Alya 與使用者之間的對話紀錄（如：關懷提醒、衛教內容紀錄） [cite: 40]。
