# NeuroLogic
# 🤖 المساعد الفلاحي الذكي (Smart Agricultural Assistant)

**الهدف** : مساعدة الفلاحين المغاربة بطريقة بسيطة باستعمال صوتهم فقط. المنصة تقوم بتسجيل السؤال، تحويله إلى نص، تحليل محتواه، ثم ترسل جواب واضح بالدارجة المغربية صوتاً ونصاً.

## 🌟 Fonctionnalités principales

- 🔐 Authentification des utilisateurs (Login / Register)
- 📄 Enregistrement des informations de la ferme
- 🎤 Assistant vocal intelligent en darija (avec transcription et synthèse vocale)
- ⛅ Intégration météo selon la localisation de la ferme
- 🧠 RAG (Retrieval-Augmented Generation) avec Pinecone
- 🧾 Backend connecté à MongoDB Atlas

---

## 🖼️ Interface Utilisateur (UI)

### 1. Authentification
![Login/Register](./assets/login.png)

### 2. Informations sur la Ferme
![Farm Info](./assets/farminfo.png)

### 3. Assistant Vocal
![Chat Assistant](./assets/chat.png)

### 4. Upload Audio et Résultat Vocal
![Audio Upload](./assets/result.png)

---

## ⚙️ Technologies utilisées

- Frontend : [Gradio](https://gradio.app/)
- NLP : Google Gemini (via `genai`)
- Vectorisation sémantique : Sentence Transformers
- RAG : Pinecone
- Base de données : MongoDB Atlas
- TTS : HuggingFace Darija Arabic TTS
- Météo : OpenWeather API

---

## 📦 Installation locale

1. Clone le repo :
```bash
git clone https://github.com/ton-repo/smart-farmer-assistant.git
cd smart-farmer-assistant
