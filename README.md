# Yorkie ASR 離線語音辨識程式

Yorkie ASR 是一款 **完全離線** 運作的語音轉文字工具，適用於所有 Windows 11 相容的硬體，**不需要使用 AI 加速卡**（如 GPU、TPU）。此程式專為個人隱私與穩定性設計，不會將任何語音資料上傳至網路，並支援多語言與語者辨識功能。

請注意: 本軟體為免費自由下載，但非開源軟體，使用者必須同意授權規範才能使用。目前仍在研發階段，品質尚未完全測試完畢，後續也會有大型更動，請勿使用於正式工作環境，否則風險必須自行承擔。

---

## 📦 安裝檔案內容

安裝程式由三個部分組成，請務必**全部下載**： https://github.com/yorkie-software/Yorkie_ASR/releases 

1. `yorkie_asr_setup.zip`
2. `yorkie_asr_setup-1.bin`
3. `yorkie_asr_setup-2.bin`

---

## 🛠️ 安裝步驟

1. 將三個檔案放在**同一個資料夾**內。
2. 解壓縮 `yorkie_asr_setup.zip`，您將看到主安裝程式: `yorkie_asr_setup.exe`。
3. **執行安裝程式**，依照畫面指示完成安裝流程。
4. 安裝完成後，即可從桌面或開始選單啟動 Yorkie ASR。

---

## 💡 程式特色

- 🖥️ **純離線執行**：無需連接網路，保護個人隱私
- 🎙️ **內建錄音功能**：可直接使用電腦麥克風錄音，錄完立即進行語音轉文字
- 🗣️ **支援語者辨識**：最多可自動區分 10 位不同人聲，標示每段語音的講者
- 🌐 **多語辨識**：支援中文、英文、日文與韓語
- 📃 **逐字稿彙總與摘要功能**：
  - 🔗 可選擇使用 **線上 Grok 服務（需連網）**
  - 💻 或使用內建的 **Google Gemma 3 4B 離線模型**
- 💾 **輕量化設計**：無需專用 GPU，執行速度快
- 🔊 **支援語音格式限制**：僅支援 **16000Hz 單通道（mono）WAV 格式**
- 📂 **轉錄輸出清晰**：輸出為 UTF-8 `.txt` 純文字檔案，可供進一步處理

---

## 📋 系統需求

- 作業系統：Windows 11
- CPU：支援 x64 架構之主流處理器
- 記憶體：建議 8 GB 以上
- 硬碟空間：安裝後約需 3 GB（含離線彙總模型）
- 不需任何 AI 或 GPU 加速器
- 彙總功能如使用 Grok 服務需具備網路連線

---

## ❓ 常見問題

**Q:** 這個軟體可以免費使用？  
**A:** 是的，免費使用之外也歡迎對外散布安裝程式。請注意: 本軟體非開源軟體，使用者必須同意授權規範才能使用。

**Q:** 安裝後是否需要網路連線？  
**A:** 語音辨識本身完全離線，僅在使用 Grok 彙總服務時需網路。

**Q:** 可以處理哪些音訊格式？  
**A:** 僅支援 **WAV 格式，取樣率為 16000Hz、單聲道（mono）**。請先使用轉檔工具（如 Audacity）轉換格式再進行辨識。由於尚在研發中，目前轉役音檔長度限制於15分鐘之內。

**Q:** 逐字稿彙總與摘要是怎麼做的？  
**A:** 可選擇：
- 線上使用 **Grok 服務**，即時產出摘要（需網路）
- 離線使用 **Gemma 3 4B 模型**，於本機進行摘要運算（包含在安裝程式中），Gemma 模型的使用授權請參閱 https://ai.google.dev/gemma/terms ，llama.cpp 使用MIT授權模式，授權聲明置於本檔最後。

---

## 🎧 音檔格式轉換說明（必須符合輸入格式）

Yorkie ASR 僅支援 **16000Hz、單聲道、WAV 格式** 的音訊輸入。如果您的原始音檔為 MP3、M4A 等其他格式，請先轉檔。

### 方法一：使用 Audacity（圖形介面，建議）

1. 下載 Audacity：[https://www.audacityteam.org](https://www.audacityteam.org)
2. 開啟 Audacity 並匯入音訊檔
3. 選取 `音軌 > 混成 > 混成至單聲道`
4. 左下角選擇 `16000 Hz`
5. 點選 `檔案 > 匯出 > 匯出為 WAV`，格式選擇 `WAV (Microsoft) 16-bit PCM`

### 方法二：使用 FFmpeg（指令列工具）

安裝 FFmpeg 後，執行以下指令：

ffmpeg -i input.mp3 -ac 1 -ar 16000 output.wav

---
Bug 或建議: https://github.com/yorkie-software/Yorkie_ASR/issues 

---

## 🐾 關於 Yorkie Software

Yorkie Software 致力於開發穩定、私密、安全的AI民主化技術產品，提供高品質的裝置端AI解決方案。

---
MIT License

Copyright (c) 2023-2024 The ggml authors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:



