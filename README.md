# 🤖 OpenHomeRobot
### *“When AI leaves the cloud and walks among us.”*

OpenHomeRobot is an open, experimental journey to bring **Large Language Models (LLMs)** to life —  
not just as chatbots, but as **humanoid companions** that can see, move, listen, and act in the real world.

This project explores how **public and self-hosted AI models** can control **physical robots** through a middleware called the **MCP Server (Model Context Protocol)** — turning language into motion, one command at a time.

---

## 🚀 Vision

The long-term goal is to make humanoid robotics accessible and intelligent enough for **home use**, starting with affordable platforms and open tools.

While Tesla Optimus and Boston Dynamics are out of budget for now, OpenHomeRobot prepares the ground for a future where **Noetix Bumi** or similar humanoids can help with real-world household tasks — controlled by private, self-hosted AI brains.

---

## 🧩 Project Phases

### **Phase 1 — LEGO Mindstorms + Public LLM**
- Hardware: LEGO **Mindstorms EV3 (31313)** and **Robot Inventor (51515)** kits  
- Software: MCP Server (Python / WebSocket / MQTT)  
- AI Brain: GPT-5 or other public LLM APIs  
- Functionality:
  - Voice input → LLM interpretation → robot motion commands
  - AI listens to voice commands and responds conversationally
  - Robot movements triggered via MCP commands (arms, legs, head)
  - Optional camera and LCD sensor upgrades for visual interaction

```
User (voice) → Speech-to-Text → LLM (AI Brain)
→ MCP Server → Robot (Mindstorms) → Real-world action
```

---

### **Phase 2 — Hiwonder AiNex**
- Next step: experimenting with the **Hiwonder AiNex humanoid robot**
- Educational use: teaching robotics and AI embodiment
- Features:
  - Visual recognition via onboard camera
  - Integration with local/private LLMs
  - Gesture-based interactions
- Objective: build a bridge between AI reasoning and human-like motion control

---

### **Phase 3 — Noetix Bumi (Dream Stage)**
- Goal: achieve **real-world humanoid operation**
- Target robot: **Noetix Robotics Bumi**
- Control approach:
  - Self-hosted **Ollama LLM** as private AI brain
  - **MCP Server** handles motion, sensory input, and feedback loops
  - Full offline/local capability — no dependency on U.S. or China-based cloud AI
- Vision: a personal humanoid that can help with household tasks, conversation, and learning

---

## ⚙️ Architecture Overview

```plaintext
         ┌───────────────────────┐
         │  User (Voice / Text)  │
         └──────────┬────────────┘
                    │
        ┌───────────▼───────────┐
        │   LLM Brain (GPT /    │
        │   Ollama / Local AI)  │
        └───────────┬───────────┘
                    │
         ┌──────────▼───────────┐
         │  MCP Server (Python) │
         │ - Motion Control     │
         │ - Command Routing    │
         │ - Sensor Feedback    │
         └──────────┬───────────┘
                    │
     ┌──────────────▼──────────────┐
     │   Robot Platform Layer      │
     │  (LEGO / AiNex / Bumi)      │
     └─────────────────────────────┘
```

---

## 🧠 The MCP Server
The **Model Context Protocol (MCP)** server acts as a bridge between the AI brain and the robot.  
It translates high-level natural language intents into low-level motion commands:

| AI Command | MCP Action | Example |
|-------------|-------------|----------|
| “Raise your right arm.” | `MOVE_ARM(right, 45°)` | Robot raises arm |
| “Walk forward.” | `MOVE_LEGS(forward, 3 steps)` | Robot walks |
| “Look at me.” | `CAMERA_TRACK(face)` | Camera follows user |

---

## 🗣️ Communication Loop

1. You speak or type a command.  
2. The AI brain (LLM) interprets intent and generates structured MCP commands.  
3. The MCP server routes commands to the robot hardware controller.  
4. The robot performs the motion and sends sensor feedback back to the LLM.  
5. The AI responds conversationally, maintaining awareness of context and environment.

---

## 🛡️ Privacy & Ethics

- AI runs locally when possible (via **Ollama** or **LAN-based inference**)
- No continuous cloud dependency
- Transparent command logging and local overrides for safety
- The project promotes **responsible and explainable AI robotics**

---

## 🌍 Inspiration

This project builds upon decades of curiosity — from LEGO robotics to modern AI embodiment.  
It’s a playground for creators, educators, and dreamers exploring how **AI can coexist with humans** in a tangible, helpful way.

---

## 🧩 Contributions

OpenHomeRobot is open for collaboration.  
We’re building the bridge between **AI and motion**, **speech and gesture**, **software and the soul of the machine**.

---

## 📅 Roadmap

- [x] Define MCP architecture  
- [x] LLM + Mindstorms integration prototype  
- [ ] Add voice and TTS support  
- [ ] Integrate AiNex humanoid  
- [ ] Ollama-based local LLM control  
- [ ] Noetix Bumi support  
- [ ] Publish open SDK for humanoid AI control

---

## ❤️ Acknowledgments

Thanks to:
- The open-source robotics community  
- LEGO, Hiwonder, and Noetix Robotics for their inspiring platforms  
- OpenAI and Ollama for making AI accessible  
- Everyone who believes AI can make our lives richer, not harder

---

**Author:** Attila Macskasy
**Lab:** [AtAIla.com](https://ataila.com)
**Blog:** [cloudmigration.blog](https://cloudmigration.blog)  
**License:** MIT  
**Status:** ⚙️ Early Experimental
