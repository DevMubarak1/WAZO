# Wazo

> Voice assistant that actually understands Nigerian languages. Runs on local hardware, not the cloud.

Wazo (Yoruba for "wisdom") is a voice assistant built for Nigeria's 200+ million people who speak Yoruba, Igbo, Hausa, and Pidgin. Unlike Siri or Alexa, everything runs locally on a Raspberry Pi in your home - no internet required, no cloud servers, complete privacy.

## Why This Exists

Try asking Alexa something in Pidgin. Or with a Nigerian accent. Doesn't work, right?

Global tech companies train their voice assistants on American and British English. They don't understand our accents, can't speak our languages, and definitely don't get our cultural context. Plus they need constant internet (good luck with that in Nigeria) and die during power outages.

So we're building something different:

- **Local AI processing** - Raspberry Pi 4 does all the work, no cloud needed
- **Nigerian-trained models** - Whisper fine-tuned on actual Nigerian speech
- **Battery backup** - Works through NEPA outages
- **Privacy first** - Your voice data never leaves your house
- **Open source** - MIT license, fork it and make it yours

## How It Works

**Hardware:**
- ESP32-S3 devices scattered around your house (microphones + speakers + LEDs)
- Raspberry Pi 4 as the "brain" running all the AI models
- Everything talks over WebSocket (local network only)

**Software Stack:**
- **Speech-to-Text**: OpenAI Whisper fine-tuned on Nigerian accents
- **Brain**: Llama-3 or Mistral running via Ollama
- **Text-to-Speech**: Coqui TTS with Nigerian voice models
- **Communication**: MCP protocol for device control

---

## Project Status & Roadmap

### Phase 1: Hardware Foundation 
- ESP32-S3 PCB design (adapted from Xiaozhi)
- Dual microphone I²S array
- Battery management system
- 3D-printed enclosure
- MCP protocol implementation

### Phase 2: Nigerian AI Models
- Fine-tune Whisper on Nigerian Pidgin
- Collect 100+ hours Nigerian voice samples
- Train Yorùbá wake word models
- Test tonal recognition accuracy
- Develop Nigerian cultural context prompts

### Phase 3: Raspberry Pi Server 
-  Build WebSocket server architecture
-  Integrate Ollama + Whisper + Coqui
-  Implement MCP device discovery
-  Create Nigerian smart home tools
-  Deploy in test households

### Phase 4: Community Testing
-  Deploy 10 units in Lagos/Ibadan/Kano
-  Gather user feedback from Nigerian users
## Current Status

**What works:**
- Hardware design (adapted from the excellent Xiaozhi ESP32 project)
- Basic firmware and audio processing
- MCP protocol communication

**What's in progress:**
- Training Whisper on Nigerian Pidgin speech
- Collecting voice samples from Nigerian speakers
- Building the Raspberry Pi server software

**What's next:**
- Wake word detection for Nigerian languages (starting with Pidgin)
- Tonal language support for Yoruba
- Deploy test units in Lagos and Ibadans. 2000mAh for frequent power outages
- **Improved ventilation** in enclosure for tropical climate

### PCB Design Files

 **Complete hardware design files in [`Hardware/`](Hardware/) directory:**
- KiCAD schematic (.kicad_sch) - Full circuit design
- KiCAD PCB layout (.kicad_pcb) - Board layout
- Gerber files - Ready for manufacturing (JLCPCB/PCBWay)
- Bill of Materials (BOM.xlsx) - Complete parts list
- 3D enclosure STL files - For FDM printing
- PDF schematics

**💡 Manufacturing**: Upload Gerber ZIP to JLCPCB, PCBWay, or AllPCB (~$15 for 5 boards)

---
## Hardware

The ESP32-S3 design is adapted from the [Xiaozhi project](https://github.com/78/xiaozhi-esp32) (huge thanks to them for open-sourcing everything). We've modified it for Nigerian conditions:

- Bigger battery (5000mAh instead of 2000mAh) because of NEPA
- Better ventilation for our climate
- Solar charging option (experimenting)

**Cost per unit:** About $40 for the ESP32 satellite, plus $55 for a Raspberry Pi 4 that can handle multiple rooms.

All design files are in the `Hardware/` folder - KiCAD schematics, PCB layouts, Gerber files ready for JLCPCB. You can build this yourself.
sudo apt update && sudo apt upgrade -y
sudo apt install -y python3-pip python3-venv portaudio19-dev ffmpeg



### Wazo License
This project is licensed under the **MIT License** - see [LICENSE](LICENSE) file for details.

### 🙏 Attribution & Acknowledgments

**Wazo builds upon excellent open-source work:**

#### Hardware & Firmware Base
- **[Xiaozhi ESP32 Project](https://github.com/78/xiaozhi-esp32)** (MIT License)
  - ESP32-S3 firmware foundation
  - MCP protocol implementation
  - Audio processing pipeline
## Nigerian Languages

Right now we're focusing on Nigerian Pidgin and Nigerian English. Yoruba, Igbo, and Hausa are coming next.

The tricky part with Yoruba is the tones - same word with different pitch means completely different things (igbá = garden, ìgbà = time, igba = calabash). We're working on training models that understand this.

*Building technology that speaks our language, not the other way around.*