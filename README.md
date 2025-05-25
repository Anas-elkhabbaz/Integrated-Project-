# NeuroLogic
# 🤖 المساعد الفلاحي الذكي (Smart Agricultural Assistant)

**هدف المشروع**: توفير مساعد ذكي للفلاحين المغاربة يمكنهم من طرح أسئلتهم بالصوت (بالدارجة المغربية)، والحصول على إجابة مفهومة وسهلة، **نصاً وصوتاً**، مع مراعاة موقع المزرعة، نوع التربة، والطقس.

---

## ⚙️ Fonctionnement général

1. ✅ L’utilisateur s’enregistre ou se connecte (MongoDB Atlas).
2. 🌾 Il fournit les informations sur sa ferme (localisation, type de sol, source d’eau...).
3. 🎤 Il envoie un fichier audio avec une question en darija.
4. 🧠 Le système :
   - Transcrit l’audio en texte avec Google Gemini
   - Récupère la météo actuelle via OpenWeather
   - Cherche des informations pertinentes avec Pinecone (RAG)
   - Construit un prompt personnalisé avec les données de la ferme
   - Génère une réponse claire et simplifiée (Google Gemini)
   - Convertit la réponse en **audio darija** grâce à un modèle HuggingFace TTS
5. 📢 La réponse est retournée sous deux formats :
   - ✅ Texte lisible
   - 🔊 Fichier audio en darija à écouter

---

## 🧪 Exemple d'utilisation

```python
audio_path = "question.wav"
username = "farmer01"

text_response, audio_file = process_audio(audio_path, username)

print(text_response)
# 🔊 audio_file est le chemin du fichier mp3 contenant la réponse vocale

