# 🛡️ Overwatch-ChipAI — Visual Reconnaissance for IoT/OT Hardware

> 🎯 An AI-powered CLI agent to analyze chip surfaces, detect debug ports, and uncover physical attack surfaces — before attackers do.

**Overwatch-ChipAI** is a terminal-based reconnaissance tool built on GPT-4.1 Vision. It scans high-resolution images of IoT/OT hardware to identify chip types, interface points (JTAG, UART, SPI), and provides vulnerability analysis based on visual layout.

---

## 🧠 Why?

Chip surfaces are the new attack surface. Debug ports, silkscreen markings, unprotected firmware interfaces — all may open doors.

This tool simulates the eyes of a seasoned hardware hacker. It helps defenders spot what they might otherwise miss.

---

## 🔧 Features

- 🤖 GPT-4.1 Vision-powered chip & PCB analysis
- 🔬 Pin/interface inference: UART, JTAG, SPI, I2C, SWD etc.
- 🧩 AI-based vulnerability assessment
- 💬 Interactive Q&A (post-analysis)
- 🎨 Rich CLI output (with `rich`)
- 📦 Auto JSON export of results
- 🛠 Manual override panel for expert hints

---

## 🛠️ Installation & Setup

### 1. 📦 Dependencies
Make sure you have Python 3.9+ and `pip` installed. Then, install required libraries:

```bash
pip install -r requirements.txt
```

If you don’t have a requirements.txt, you can also install manually:

```bash
pip install openai opencv-python rich numpy
```

### 2. 🔑 Set Your OpenAI API Key
You can either:

a) Use environment variable:
```bash
export OPENAI_API_KEY="sk-..."
```
b) Or hardcode inside:
```bash
openai.api_key = "your-api-key"
```

## 🚀 Usage

```bash
python3 SelfHack_Overwatch-ChipAI.py path/to/your_chip.jpg
```
You’ll get a structured vulnerability analysis based on chip layout, labels, and component positioning.

## 💡 Sample Output
<img width="2982" height="1798" alt="image" src="https://github.com/user-attachments/assets/11a16b8e-45f2-43ce-8dfd-310b05a035b8" />
<img width="2104" height="1598" alt="image" src="https://github.com/user-attachments/assets/7aa4a90b-65f8-4b78-8df9-405a43ab0b66" />

## 💬 Chat Mode
After the AI responds, you’ll be prompted for interactive Q&A:

```bash
> What happens if I inject 5V on pin 3?
🤖: That pin appears to be VOUT. Overvoltage injection could bypass regulation...
```

## 🧠 System Prompt Logic
-The built-in prompt simulates:
-A seasoned hardware reverse engineer
-Knowledge of physical + firmware attack paths
-Ability to research chip markings online
-Inference based on silkscreen, layout, and common IC design

## ⚠️ Legal Note
This tool is intended for authorized testing and research purposes only.
Do not use it on hardware you do not own or have permission to analyze.

🌐 Tags
GPT-4.1 • chip-hacking • iot-research • hardware-recon • openai-vision • reverse-engineering • SelfHack AI
