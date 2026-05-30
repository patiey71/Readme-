# Readme-
CyberGuard Assistant — Part 2 (PROG6221 POE)
Overview
A WPF-based Cybersecurity Awareness Chatbot that expands Part 1 with a full GUI, dynamic keyword recognition, sentiment detection, memory/recall, conversation flow, and OOP-structured code.
Features Implemented
1. GUI Design & Implementation (WPF)
Dark-themed, colour-coded chat interface using WPF
ASCII art header rendered in Courier New
Voice greeting using System.Speech.Synthesis.SpeechSynthesizer
Timestamped messages with distinct colours for user and bot
Send on Enter key or Send button; Clear button to reset chat
2. Keyword Recognition
Recognises 10+ cybersecurity topics from user input:
password, phishing, scam, privacy, malware, ransomware, firewall, 2fa, vpn, social engineering
3. Random Responses
Each keyword has 4 predefined responses stored in a Dictionary<string, List<string>>. The chatbot randomly selects one using Random.Next() so conversations stay varied.
4. Conversation Flow
Follow-up triggers: "give me another tip", "tell me more", "explain more", etc.
Chatbot continues on the last recognised topic without restarting
Confusion/detail requests handled seamlessly
5. Memory & Recall
Stores the user's name and favourite topic in a UserMemory object
References the stored name and topic later in the conversation
Tracks topics the user has asked about and provides personalised tips
6. Sentiment Detection
Detects worried, curious, frustrated, happy sentiments from user input keywords and prepends an empathetic prefix to the response.
7. Error Handling & Edge Cases
Randomised default response for unrecognised input
No crashes on empty or unexpected input
Graceful TTS fallback if System.Speech is unavailable
8. Code Optimisation (OOP)
ChatbotEngine class encapsulates all logic
UserMemory data class for memory management
Sentiment enum for sentiment states
Dictionaries and lists for all keyword/response management
Methods are single-responsibility and named clearly
How to Run
Open CybersecurityChatbot.csproj in Visual Studio 2022 or later.
Ensure .NET 8.0 SDK (Windows) is installed.
Press F5 or click Run
