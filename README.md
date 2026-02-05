# 🤖 Automated Urdu News Generator | Tech Insights

[![Watch Demo](https://img.shields.io/badge/Watch-Demo%20Video-red?style=for-the-badge&logo=youtube)](https://drive.google.com/file/d/1cHGgVyA4a0ALhLE3Dq1xmoXs8UQdUfSE/view?usp=sharing)
[![n8n](https://img.shields.io/badge/n8n-Workflow-orange?style=for-the-badge&logo=n8n)](https://n8n.io)
[![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o-green?style=for-the-badge&logo=openai)](https://openai.com)

> **A fully autonomous AI pipeline that curates tech news, translates to Urdu, generates custom graphics, and delivers to WhatsApp — zero human intervention.**

---

## 📸 Workflow Architecture

![Tech Insight Workflow](TECH%20INSGHIT%20WORKFLOW.PNG)

---

## 🎯 What Does It Do?

This project is a **self-operating digital media agent** that:

✅ Fetches live tech news from global RSS feeds (TechCrunch, The Verge)  
✅ Uses **GPT-4o** to translate English articles into **Urdu** and summarize into 3 bullet points  
✅ Generates **studio-quality graphics** programmatically (HTML/CSS → JPEG)  
✅ Delivers final image to **WhatsApp** in under **60 seconds**  
✅ Runs **daily at 8 AM** automatically via Cron scheduling  

---

## 🎥 Demo Video

**Watch the full walkthrough here:**

[![Demo Video](https://img.shields.io/badge/▶️-Watch%20on%20Google%20Drive-4285F4?style=for-the-badge)](https://drive.google.com/file/d/1cHGgVyA4a0ALhLE3Dq1xmoXs8UQdUfSE/view?usp=sharing)

---

## 🏗️ Technical Architecture

The system is built with **4 intelligent layers**:

### **1️⃣ Data Ingestion & Normalization Layer**
- **Cron Job Trigger**: Scheduled at 8:00 AM daily
- **RSS Feed Extraction**: Pulls data from TechCrunch/The Verge
- **XML to JSON Parsing**: Converts RSS feed into machine-readable format
- **Filtering Logic**: Eliminates ads and invalid entries
- **Rate Limiting**: Selects top trending story

### **2️⃣ AI Core (NLP Processing)**
- **GPT-4o Integration**: Real-time translation (English → Urdu)
- **Semantic Summarization**: Converts articles into 3 concise bullet points
- **Structured JSON Output**: Ensures downstream compatibility
- **Error Handling**: Custom JavaScript sanitization for API responses

### **3️⃣ Dynamic Visual Rendering Engine**
- **Custom HTML/CSS Generator**: No Canva templates—pure code
- **Responsive Flexbox Layout**: Auto-adjusts based on content length
- **Premium Styling**: Linear gradients, CSS masking, Noto Nastaliq Urdu font
- **HCTI API**: Converts HTML code into high-res JPEG (650x500px)

### **4️⃣ Distribution & Delivery Layer**
- **Binary Stream Handling**: Downloads generated image
- **WhatsApp Cloud API**: Uploads media and broadcasts to community groups
- **End-to-end Latency**: < 60 seconds from news publish to delivery

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| **Orchestration** | n8n (Self-Hosted) |
| **AI Model** | OpenAI GPT-4o |
| **Languages** | JavaScript (ES6+), HTML5, CSS3 |
| **APIs** | HCTI (Image Generation), Meta WhatsApp Cloud API |
| **Hosting** | VPS (Hostinger) |
| **Scheduling** | Cron Jobs |

---

## ⚡ Key Features

🔹 **Self-Healing Architecture**: Try-catch blocks with fallback logic  
🔹 **Zero-Human Latency**: Fully autonomous execution  
🔹 **Programmatic Design**: Graphics are code, not templates—infinite scalability  
🔹 **Multi-Language Support**: English → Urdu translation via GPT-4o  
🔹 **Production Ready**: Live deployment with error handling  

---

## 🚀 How It Works

```mermaid
graph LR
    A[Cron Trigger<br/>8:00 AM] --> B[RSS Feed<br/>TechCrunch]
    B --> C[XML Parser]
    C --> D[Filter & Limit]
    D --> E[GPT-4o<br/>Translation]
    E --> F[HTML Generator]
    F --> G[HCTI API<br/>Image Render]
    G --> H[WhatsApp API<br/>Delivery]
