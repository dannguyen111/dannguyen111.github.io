---
layout: project
title: "APPC Archive Assistant"
description: "An AI-powered Retrieval-Augmented Generation (RAG) system designed to search and synthesize decades of university academic policy minutes."
image: assets/images/appc-chatbot-preview.png
tags: [AI/ML, RAG, Django, React, Python, pgvector, LLMs]
date: 2026-05-06
---

![APPC Archive Assistant Chat Interface](assets/images/appc-chatbot-preview.png)
*A preview of the APPC Archive Assistant chat interface and citation system.*

**[Try the Live Demo Here (Access to the chat is only available to Gettysburg College Faculty and Students)](http://commiteedoc.us.reclaim.cloud/chat)**

### Project Overview
The APPC Archive Assistant is an AI-powered document management system designed to help university faculty seamlessly search and analyze decades of Academic Policy and Program Committee (APPC) minutes. It operates as a sophisticated Retrieval-Augmented Generation (RAG) pipeline that drastically reduces the administrative burden of researching historical academic policy.

### System Architecture & Technical Highlights

* **Semantic Search Backend:** Built with Django, the system performs highly accurate vector similarity searches across thousands of historical meeting records and document chunks.
* **Intelligent Query Parsing:** Engineered a multi-layered natural language parser that pre-processes user queries. It extracts specific course codes, date constraints, and member attendance records to filter the database before the vector search even begins.
* **Robust LLM Synthesis:** The response engine dynamically synthesizes answers using a resilient fallback chain of top-tier low latency models (including gpt-4o-mini and Gemini 2.5 Flash). It generates strict, highly accurate answers with clickable citations that link directly back to the original source PDFs.
* **Interactive Frontend & Cost Tracking:** The client is built in React and features a responsive chat interface alongside a comprehensive admin cost-tracking dashboard. The dashboard evaluates API token usage and tracks precise generation times (latency) using multithreaded, parallel test executions.