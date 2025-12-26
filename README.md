# WAZO: An Open-Source Indigenous Nigerian Voice Assistant 🎙️🇳🇬

![Wazo Project Logo](./wazo.jpg)

**WAZO** is a decentralized, edge-AI voice assistant designed specifically for the Nigerian linguistic landscape. While global assistants (Siri, Alexa) prioritize high-resource Western languages, Wazo is purpose-built to understand and respond in **Nigerian Pidgin, Yorùbá, Igbo, and Hausa**, as well as Nigerian-accented English.

## 🌟 Why Wazo?
Over 200 million people speak Nigerian languages, yet voice technology remains largely inaccessible or biased against local accents and tonal variations. Wazo bridges this gap by:
- **Linguistic Inclusion:** Native support for the three major Nigerian languages and Pidgin.
- **Privacy & Edge Computing:** All processing happens locally on a Raspberry Pi 4—no voice data is sent to foreign cloud servers.
- **Low Latency:** Distributed architecture using ESP32 nodes for instant response.

---

## 🏗️ System Architecture

Wazo operates on a **Client-Server Edge model**:
1. **The Server (Raspberry Pi 4):** Acts as the "Brain." It hosts the heavy-duty Speech-to-Text (STT), Large Language Model (LLM), and Text-to-Speech (TTS) engines.
2. **The Satellite (ESP32):** Acts as the "Ear and Mouth." These small, affordable nodes are placed around the home to capture audio and play back Wazo’s response.

---

## 🛠️ Tech Stack

### 👂 Hearing (STT)
- **Model:** OpenAI Whisper (Fine-tuned).
- **Dataset:** [NaijaVoices](https://huggingface.co/datasets/naijavoices/naijavoices-dataset) (1,800+ hours of authentic Nigerian speech).

### 🧠 Thinking (LLM)
- **Engine:** [Ollama](https://ollama.com/) running locally on Pi 4.
- **Models:** Quantized Llama-3 or Mistral with custom system prompts for Nigerian cultural context.

### 🗣️ Speaking (TTS)
- **Model:** [YarnGPT](https://github.com/saheedniyi02/yarngpt) / Coqui TTS.
- **Output:** Natural, Nigerian-accented voices (e.g., Idera, Tayo, Chinenye).

---

## 🚀 Getting Started

### Prerequisites
- **Hardware:** Raspberry Pi 4 Model B (4GB/8GB recommended), ESP32 Microcontroller, I2S Microphone (INMP441), and Speaker.
- **OS:** Raspberry Pi OS (64-bit).

### Installation (Server)
1. Clone the repo:
   ```bash
   git clone [https://github.com/DevMubarak1/WAZO.git](https://github.com/DevMubarak1/WAZO.git)
   cd WAZO
