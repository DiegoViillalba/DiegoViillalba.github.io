---
title: "Smart Docs"
excerpt: "Intelligent document processing powered by LLMs and OCR — extract structured data from documents using modern AI pipelines. <br/><img src='/images/smart_docs.png'>"
collection: portfolio
---

## Overview

Smart Docs is an intelligent document processing system that leverages large language model (LLM) APIs and OCR techniques to extract structured data from unstructured documents such as PDFs and images.

The project is designed as a scalable, end-to-end pipeline that combines modern web technologies with AI-based perception, enabling automated parsing of invoices, forms, and contracts into clean, structured JSON outputs.

---

## Motivation

Many real-world workflows rely on manual document processing, which is time-consuming, error-prone, and difficult to scale. Smart Docs addresses this by combining:

- Vision-capable LLMs for semantic understanding  
- OCR pipelines for text extraction  
- Cloud-based infrastructure for scalability  

The goal is to build robust systems that bridge unstructured data and structured information pipelines.

---

## Key Features

- AI-powered OCR — Extract text and structured data from images and PDFs using LLM vision APIs  
- Real-time processing — Live status updates using Firebase  
- Structured extraction — Convert documents into clean JSON schemas  
- Document storage — Upload, organize, and retrieve files via Firestore  
- Authentication & permissions — Role-based access using Firebase Auth  
- Responsive UI — Fully functional across desktop and mobile  

---

## Architecture

```text
📄 Upload document
      ↓
🔥 Firebase Storage
      ↓
🧠 LLM API (vision model)
      ↓
📊 Structured JSON output
      ↓
🗄️ Firestore (storage & retrieval)
```