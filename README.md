# 🚗 EcoDrive RAG API - WatsonX AI + Railway

This repository hosts the Retrieval-Augmented Generation (RAG) backend for the **EcoDrive** project, built using IBM WatsonX AI and deployed on [Railway](https://railway.app).

The goal is to provide real-time, AI-powered **eco-driving suggestions** by querying WatsonX AI using trip and driving behavior data collected from vehicles.

---

## 🔗 Live Endpoint

**POST** `https://ecodriveragwatsonx.up.railway.app/rag`

---

## 🧠 How It Works

This RAG API receives a `query` and uses WatsonX AI to generate climate-conscious advice. The responses are fine-tuned with context like:

- Driving behavior (e.g., idling, speeding)
- Trip statistics (distance, fuel, CO₂)
- Pre-uploaded knowledge from curated vector index documents

---

## 📦 Request Format

```json
POST /rag
Content-Type: application/json

{
  "query": "I am idling for more than 20 min today, how much will it affect the climate?"
}
