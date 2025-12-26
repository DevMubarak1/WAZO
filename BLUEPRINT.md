# Blueprint Application: Wazo

## What I'm Building

A voice assistant that understands Nigerian languages. Runs entirely on local hardware - no cloud, no internet required.

Think Alexa, but for the 200+ million Nigerians who speak Yoruba, Igbo, Hausa, and Pidgin. And it works during power outages.

## The Problem

Try asking Siri something in Pidgin. Or even Nigerian English. Doesn't work.

Global voice assistants are trained on American/British accents. They:
- Don't understand our accents
- Can't handle tonal languages (Yoruba's pitch changes word meaning)
- Need constant internet (unreliable here)
- Die during power cuts (daily occurrence)
- Send your data to foreign servers

Result: 200 million people locked out of voice AI.

## My Solution

Wazo (Yoruba for "wisdom") runs everything locally:
- ESP32 devices around your house (microphone + speaker + LEDs)
- Raspberry Pi 4 as the "brain" running AI models
- No internet needed after initial setup
- Battery backup for when NEPA takes light
- Custom trained on Nigerian speech

Cost: Under $100 total. Open source hardware.

## What I'm Actually Building

**Hardware:**
- ESP32-S3 satellite units (I'm adapting the open-source Xiaozhi design)
- Modified PCB for Nigerian conditions: bigger battery (5000mAh vs 2000mAh), better ventilation, solar-ready
- 3D printed enclosures

**Software (this is the original work):**
- Raspberry Pi server replacing all cloud AI
- Whisper model fine-tuned on Nigerian speech samples
- Llama-3 running via Ollama for conversations
- Coqui TTS generating Nigerian-accented voices
- Wake word detection for all 5 languages

**Community:**
- Collect 500+ hours of real Nigerian speech
- Deploy 10 test units in Lagos, Ibadan, Kano
- Document tonal language challenges (this is novel research)
- Run maker workshops for Nigerian students

## What's From Xiaozhi vs What's Mine

**Xiaozhi gave me (their MIT-licensed work):**
- ESP32-S3 hardware design
- Audio processing firmware
- MCP protocol for devices
- 3D enclosure files

**What I'm adding (100% my work):**
- All the Nigerian language AI training
- Local Pi server architecture (Xiaozhi uses cloud)
- Hardware mods for power/climate
- Tonal language wake words
- Nigerian cultural context
- Deployment methodology

This isn't a clone - I'm using proven hardware to solve a completely different problem.

### Budget Breakdown (~$2,500)

| Item | Quantity | Cost |
|------|----------|------|
| PCB manufacturing (5 boards/order) | 2 batches | $150 |
| Electronic components (per unit) | 10 units | $370 |
| Raspberry Pi 4 (4GB) kits | 3 units | $165 |
| Li-Ion batteries (5000mAh) | 10 units | $120 |
| 3D printing filament | 10 enclosures | $80 |
| Nigerian voice data collection | 100+ hours | $500 |
|  Budget ($2,500)

- PCB manufacturing (2 batches, 5 boards each): $150
- Electronic components (10 units): $370
- Raspberry Pi 4 kits (3 units): $165
- Batteries (5000mAh, 10 units): $120
- 3D printing filament: $80
- Voice data collection (compensating speakers): $500
- Cloud GPU for training models: $400
- Travel to deploy/test in Lagos/Ibadan: $300
- Documentation/videos: $200
- Shipping & unexpected costs: $215

The expensive parts are the AI training compute and paying people fairly for voice samples.

## Timeline (7 Months)

**Months 1-2:** Assemble hardware, build Pi server  
**Months 3-4:** Train Pidgin AI models, test locally  
**Months 5-6:** Deploy to 10 homes, collect feedback  
**Month 7:** Document everything, open source release

## Why I Need Blueprint

I can't afford this myself. Specifically:
- $400 for components (10 units × $40)
- $400 for GPU training time
- $500 to fairly compensate voice contributors
- $300 for travel to different cities

This isn't just another voice assistant. It's about linguistic justice - proving that tech can work for everyone, not just English speakers.ud connection (unreliable in Nigeria), and don't work during power outages (70%+ of the day). We need local, power-resilient solutions.

**Q: Can you really train AI models as a student?**  
A: Yes! Whisper fine-tuning is well-documented, Ollama runs on Pi 4, and Coqui TTS is open-source. We're not building models from scratch - we're adapting existing ones with Nigerian data.

**Q: What if you don't finish?**  
A: Minimum viable product is Nigerian Pidgin working on 3 units. That alone proves the concept and helps 200M+ people. Yorùbá/Igbo/Hausa can follow in iterations.

---

**This is more than a hardware project - it's a statement that African languages deserve voice AI too.** 🇳🇬
## What Success Looks Like

- 10 working units in Nigerian homes
- 90%+ wake word accuracy for Pidgin
- 500+ hours of speech data published for researchers
- Everything open sourced (MIT license)
- Proof this works for other African languages

Minimum viable: Even just Pidgin working on 3 units proves the concept for 200+ million speakers.

## Open Source Promise

Everything will be MIT licensed:
- All code on GitHub
- KiCAD files and Gerbers
- Voice datasets (for research)
- Full attribution to Xiaozhi
- Documentation for other countries to adapt

## Links

- **GitHub**: https://github.com/yourusername/wazo
- **Hardware**: See `/Hardware` folder
- **Base project**: https://github.com/78/xiaozhi-esp32

---## Anticipated Questions

**"Is this just copying Xiaozhi?"**  
No. Xiaozhi is cloud-based and doesn't support any African languages. I'm using their open-source hardware (which is awesome) but doing completely original work on Nigerian AI, local server setup, and cultural adaptation. The value is making it work for underserved languages.

**"Why not just use Google/Alexa?"**  
They don't understand Nigerian languages, need constant internet (unreliable here), and die during our daily power outages. We need local, power-resilient solutions.

**"Can you actually train AI models as a student?"**  
Yes. Whisper fine-tuning is well documented. Ollama runs on Pi 4. Coqui TTS is open source. I'm not building models from scratch - adapting existing ones with Nigerian data.

**"What if you don't finish everything?"**  
Minimum viable product is Pidgin working on 3 units. That alone helps 200M+ people and proves the concept. The other languages can come in iterations.

---

*More than a hardware project - it's a statement that African languages deserve voice AI too.*