# 🌤️ Morning Weather & Trail Dashboard (n8n + OpenAI Agent)

This repository showcases an automated **daily weather and trail dashboard email** created using **n8n**, **OpenAI AI Agent**, **Google Calendar**, **Google Sheets**, **OpenWeather**, and **Gmail**.  
The system runs every morning and emails a clean, line-by-line weather dashboard, and if a trail event is scheduled for today, it recommends the best possible trail based on weather conditions.

---

## ✨ Features

- ⏰ **Daily 5:00 AM automation**
- 🌤️ **Real-time weather dashboard**
- 🧠 **AI-powered reasoning using OpenAI Agent**
- 📅 **Reads Google Calendar trail events**
- 🥾 **Trail recommendations from Google Sheets**
- 🚫 **No recommendation if weather is unsafe**
- 📧 **Sends clean, emoji-styled dashboard email**

---

## 🧠 How It Works (High-Level Architecture)

Schedule Trigger
↓
AI Agent
↓
┌───────────────┬───────────────┬────────────────┐
│ Check Calendar│ Get Weather │ Get Trail List│
└───────────────┴───────────────┴────────────────┘
↓
Send Email (Gmail)

yaml
Copy code

- **Schedule Trigger** runs daily at a set time (e.g., 5:00 AM)
- **AI Agent** formats the dashboard + makes trail decisions
- **Check Calendar** checks if the user has a trail event today
- **Get Weather** fetches live weather from OpenWeather
- **Get Trail List** reads trails from Google Sheets
- **Send Email** sends the final dashboard to Gmail

---

## 📸 Screenshots

### n8n Workflow  
<img src="Weather Update Workflow.png" width="700"/>

### Email Output  
<img src="Test Email.png" width="700"/>

---

## 📁 Repository Structure

.
├── README.md
├── Test Email.png
├── Weather Update Workflow.png
└── workflow
└── scheduled-weather-update.json

yaml
Copy code

---

## 🚀 How to Use This Workflow

### 1️⃣ Install or open **n8n**
You can use:
- n8n Cloud  
- n8n Desktop  
- Local Docker setup

### 2️⃣ Import the workflow
Download the file:
workflow/scheduled-weather-update.json

yaml
Copy code
Then in n8n:
Menu → Import → Select JSON file

yaml
Copy code

### 3️⃣ Add your credentials
Inside the workflow, configure:

- **OpenAI** (AI agent)
- **Google Calendar**
- **Google Sheets**
- **OpenWeather API**
- **Gmail**

### 4️⃣ Update the Google Sheet reference
In the **Get Trail List** node:
- Enter your sheet ID  
- Set tab name (e.g., "Runs")  
- Set range if needed  

### 5️⃣ Activate the workflow
Set your preferred time in the Schedule Trigger (e.g., 05:00) and enable it.

You’ll now receive your **Morning Weather Dashboard email** automatically every day.

---

## 🧾 Technologies Used

- **n8n** (automation engine)  
- **OpenAI GPT-4o-mini** (AI Agent)  
- **Google Calendar API**  
- **Google Sheets API**  
- **OpenWeather API**  
- **Gmail API**  
- **JavaScript-based n8n node processing**  

---

## 🎯 Purpose of the Project

This project was created to demonstrate:

- AI-powered workflow design  
- Automation engineering  
- API integrations  
- Prompt engineering  
- Real-world useful automation  

It’s a strong portfolio project for roles in:
- Automation Engineering  
- AI Integration  
- Backend Workflow Systems (n8n)  
- Cloud Automation  
- Technical Product Engineering  

---

## 📄 License
MIT — free to use, modify, and adapt.

---
