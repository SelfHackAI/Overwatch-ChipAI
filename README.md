# 🛡️ Overwatch-ChipAI — Visual Reconnaissance for IoT/OT Hardware

<img width="1918" height="321" alt="image" src="https://github.com/user-attachments/assets/5eeea057-13d9-4502-8327-dfa64af3f8f0" />

A single-file tool that analyzes PCB images using GPT-4.1, OCR, and online datasheet lookup.  
Extracts IC markings, finds public datasheet links, and performs AI-based hardware security analysis — all with one command.

---

## 🚀 Features

- 📷 OCR to extract chip markings from PCB photos  
- 🌍 Searches Google for real datasheet links (for reference only)  
- 🤖 GPT-4.1 analyzes the image + markings to determine component roles  
- 🧷 Identifies potential attack surfaces (UART, JTAG, SWD, etc.)  
- 📋 Summary tables displayed in terminal (components, surfaces, suggestions)  
- 💬 Interactive Q&A mode with GPT  
- 💾 Exports full results to `ai_chip_analysis.json`

---

## 📦 Requirements

```bash
pip install openai opencv-python numpy pytesseract requests beautifulsoup4 rich
```

Install Tesseract OCR:

- **macOS:** `brew install tesseract`
- **Ubuntu:** `sudo apt install tesseract-ocr`
- **Windows:** https://github.com/UB-Mannheim/tesseract/wiki

---

## 🔑 OpenAI API Key

Set it inside the script:

```python
openai.api_key = "sk-..."
```

or use environment variable:

```bash
export OPENAI_API_KEY="sk-..."
```

---

## 🧠 Usage

```bash
python selfhack_Overwatch-ChipAI.py my_pcb.jpg
```

You will see:
- OCR-extracted chip IDs
- Datasheet links
- GPT-4.1 AI analysis
- Terminal summary tables
- JSON output
- Live Q&A chat

---

## 📚 Example Output

<img width="1932" height="844" alt="image" src="https://github.com/user-attachments/assets/2094a70e-0eb4-4319-b6f1-5c8f460b92b1" />
<img width="2574" height="1474" alt="image" src="https://github.com/user-attachments/assets/e12f9efa-3465-46b3-8155-885cf4d7589e" />
<img width="2342" height="1602" alt="image" src="https://github.com/user-attachments/assets/6d9e6e5b-d796-48bf-978e-b6b2388ffbf5" />
<img width="3530" height="172" alt="image" src="https://github.com/user-attachments/assets/d0838bf0-07ba-4a92-a0ab-d456603cfbb9" />

---

## 💬 Q&A Chat Mode

```text
> What is the flash chip?
🤖 Likely a 25Q32 SPI flash near the MCU.

> Any RF module detected?
🤖 No RF chip detected in the OCR results.
```
---

## 📜 License

This project is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

You are free to use, modify, and distribute this software under the terms of this license.

Built by [SelfHack AI](https://selfhack.ai)


## ⚠️ Legal Note
This tool is intended for authorized testing and research purposes only.
Do not use it on hardware you do not own or have permission to analyze.

🌐 Tags
GPT-4.1 • chip-hacking • iot-research • hardware-recon • openai-vision • reverse-engineering • SelfHack AI
