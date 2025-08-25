# 🎙️ Murf_ai 

This project is a hands-on guide to building a **voice-based conversational AI** using modern web technologies and powerful AI APIs. You can engage in a **continuous, voice-to-voice conversation** with an AI powered by **Google's Gemini LLM**. The agent remembers the context of your conversation, enabling natural follow-up questions and a more human-like interaction.  

The repository is structured by **day**, with each folder representing a significant step in the development process — from setting up the server to implementing a **full conversational loop with memory**.  

---

## ✨ Key Features  
- **Voice-to-Voice Interaction**: Speak to the agent and receive a spoken response for a seamless conversational experience.  
- **Contextual Conversations**: Maintains a chat history per session, enabling intelligent follow-ups.  
- **End-to-End AI Pipeline**: Integrates Speech-to-Text → LLM → Text-to-Speech in one flow.  
- **Modern & Intuitive UI**: Clean, single-button interface with visual feedback (ready, recording, thinking).  
- **Robust Error Handling**: Includes fallback audio responses for smooth user experience when API calls fail.  

---

## 🛠️ Tech Stack  

**Backend:**  
- [FastAPI](https://fastapi.tiangolo.com/) – High-performance, async API server  
- [Uvicorn](https://www.uvicorn.org/) – ASGI server for FastAPI  
- [Python-Dotenv](https://pypi.org/project/python-dotenv/) – Manage environment variables securely  

**Frontend:**  
- HTML, CSS, JavaScript  
- [Bootstrap](https://getbootstrap.com/) – Responsive UI components  
- MediaRecorder API – Capture microphone audio in the browser  

**AI & Voice APIs:**  
- [Murf AI](https://murf.ai/) – High-quality Text-to-Speech (TTS)  
- [AssemblyAI](https://www.assemblyai.com/) – Accurate Speech-to-Text (STT)  
- [Google Gemini](https://deepmind.google/technologies/gemini/) – LLM for intelligent responses  

---

## ⚙️ Architecture  

The application follows a **client-server architecture**:  

1. **Client (Browser)**  
   - Captures voice input with the MediaRecorder API  
   - Sends audio to the backend  
   - Plays the AI’s spoken response  
   - Updates UI states (ready, recording, thinking)  

2. **Server (FastAPI)**  
   - Receives audio input  
   - Sends audio → **AssemblyAI** (STT)  
   - Retrieves chat history & sends context → **Google Gemini** (LLM)  
   - Sends Gemini’s response → **Murf AI** (TTS)  
   - Returns final audio URL to the client  



