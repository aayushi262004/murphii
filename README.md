🎙️ Murf_ai

An AI-powered conversational voice agent that listens, understands, and responds in real-time using STT (Speech-to-Text), LLM (Language Model), and TTS (Text-to-Speech).

✨ Features

🎤 Speech Recognition – Converts spoken input into text using AssemblyAI.

🧠 Conversational AI – Generates intelligent responses with Gemini LLM.

🔊 Voice Output – Speaks responses naturally using Murf AI voices.

⚡ Real-Time Communication – Powered by FastAPI and WebSockets.

🛠️ Tech Stack

Backend:
FastAPI: For building the high-performance, asynchronous API server.
Uvicorn: As the ASGI server to run the FastAPI application.
Python-Dotenv: To manage environment variables securely.

Frontend:
HTML, CSS, JavaScript: For the structure, styling, and client-side logic.
Bootstrap: For creating a responsive and modern user interface.
MediaRecorder API: To capture audio directly from the user's microphone in the browser.

AI & Voice APIs:
Murf AI: For generating high-quality, natural-sounding Text-to-Speech (TTS).
AssemblyAI: For providing fast and accurate Speech-to-Text (STT) transcription.
Google Gemini: As the Large Language Model (LLM) for generating intelligent and coherent responses.

🚀 Getting Started
1️⃣ Clone the repository
git clone https://github.com/your-username/ai-voice-agent.git
cd ai-voice-agent

2️⃣ Install dependencies
pip install -r requirements.txt

3️⃣ Set up environment variables

Create a .env file in the root directory with your API keys:

ASSEMBLYAI_API_KEY=your_key_here
GEMINI_API_KEY=your_key_here
MURF_API_KEY=your_key_here

4️⃣ Run the server
uvicorn main:app --reload

5️⃣ Open the app

Visit http://127.0.0.1:8000 in your browser.

📂 Project Structure
ai-voice-agent/
│── app/
│   ├── main.py          # FastAPI entry point
│   ├── services/        # STT, LLM, TTS services
│   ├── static/          # Frontend JS, CSS
│   └── templates/       # HTML UI
│── .env.example         # Example env file
│── requirements.txt     # Python dependencies
│── README.md            # Project documentation
