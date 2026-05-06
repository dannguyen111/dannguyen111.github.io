---
layout: project
title: "TwinMind Copilot"
description: "An AI-powered live meeting assistant that transcribes speech in real-time, generates contextual suggestions, and features an interactive deep-dive chat."
image: assets/images/twinmind-preview.png
tags: [AI/ML, React, Django, Python, Groq API, LLMs, Docker]
date: 2026-05-06
---

**[Try the Live Demo Here](https://twinmind-live-suggestions-xi.vercel.app/)**

### Project Overview
TwinMind Copilot is an elite, AI-powered live meeting assistant designed to enhance productivity and comprehension during discussions. It listens to microphone audio, transcribes speech in real-time, generates instantly actionable suggestions (such as questions to ask or fact-checks), and provides a context-aware chat interface to dive deeper into any topic discussed during the meeting. 

### System Architecture & Technical Highlights

* **Real-Time Audio Processing:** Captures and batches microphone audio, transcribing it accurately with ultra-low latency using Groq's Whisper model (`whisper-large-v3`).
* **Contextual AI Decision Engine:** Analyzes live transcripts using `llama3-70b-8192` to dynamically generate color-coded, actionable insights. The system "reads the room" to provide the right mix of Questions, Talking Points, Answers, Fact-Checks, or Clarifications based on the immediate conversational context.
* **Interactive Context-Aware Chat:** Features a unified chat interface where users can click on live suggestions for comprehensive markdown-formatted deep dives, or type manual follow-up questions. It utilizes a smart context window that intelligently truncates older history to optimize token payloads.
* **Full-Stack Split Deployment:** Built with a React/Vite frontend hosted on Vercel and a containerized Python/Django REST API backend deployed globally on Fly.io, connected securely via strict CORS configurations.
* **Dynamic Settings Management:** Includes a built-in UI to customize LLM system prompts and character limits on the fly, saving configurations seamlessly in the browser's local storage.