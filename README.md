# whatsfordinner
AI dinner planner 
🧠 Meal Suggestion GPT Assistant

A simple AI-powered meal suggestion chatbot built with **Next.js**, **OpenAI GPT-4o**, and deployed via **Vercel**.

This tool helps generate dinner ideas based on:
- What ingredients you currently have
- What you feel like eating
- Your personalized dietary restrictions and preferences (e.g. no onions, no soups, easy meals)

## 🚀 Live Prompt: “What’s for dinner tonight?”

---

## 🧱 Features

- Serverless API route (`/api/chat`) that calls OpenAI GPT-4o
- Injects a structured diet plan stored in a local JSON file
- Filters out unwanted meals (e.g. soup, onions)
- Suggests 2–3 easy, healthy recipes under 40 minutes
- Clean and customizable base for extending to a chat UI

---

## 🗂 Project Structure

app/
├── api/
│ └── chat/
│ └── route.ts # OpenAI-powered meal suggestion logic
├── data/
│ └── diet_plan_with_preferences.json # User’s dietary rules

yaml
Copy
Edit

---

## ⚙️ Setup Instructions

### 1. Clone the repo

```bash
git clone https://github.com/yourusername/meal-suggestion-gpt.git
cd meal-suggestion-gpt
2. Install dependencies
bash
Copy
Edit
npm install
3. Add your OpenAI API key
Create a .env.local file at the root:

bash
Copy
Edit
OPENAI_API_KEY=sk-xxxxxxx
4. Run locally
bash
Copy
Edit
npm run dev
Send a POST request to http://localhost:3000/api/chat with this body:

json
Copy
Edit
{
  "ingredients": "zucchini, tuna, rice",
  "feeling": "something fresh and easy"
}
☁️ Deploy to Vercel
Push the repo to GitHub.

Go to vercel.com and import your project.

In Project Settings → Environment Variables, add:

ini
Copy
Edit
OPENAI_API_KEY = sk-xxxxxx
Click Deploy!

📄 License
MIT – feel free to customize and extend!

yaml
Copy
Edit

---

Let me know if you'd like:
- A pre-filled GitHub template version of this
- Help wiring up a frontend UI for it
- Or a GitHub Action to auto-deploy on push to Vercel!
