# 🎭 AutoStory Generator (Airtable + AI)  
_Automated Profile → Rating → Story Generator using Airtable, n8n & Gemini AI_

<img width="825" height="340" alt="Story Making Agent" src="https://github.com/user-attachments/assets/408e6c29-3b6d-4073-852a-6be649a22a90" />

## 📌 Overview
AutoStory Generator (Airtable + AI) Agent is an automated workflow that converts simple user-submitted form data into:

- ⭐ Profession-based rating  
- ✍️ An AI-generated poem/story about the person  
- 🗃️ Auto-updated records inside Airtable  

This workflow is built using **n8n**, **Airtable**, and **Google Gemini AI**, and is triggered every time a user submits a form containing their **Name**, **Looks**, and **Profession**.

---

## 🚀 How It Works

### **1. User Submits the Form**
The form contains three fields:
- **Name** – e.g., `John`
- **Looks** – e.g., `Tall & Handsome`
- **Profession** – (dropdown)
  - `Video Editing`
  - `Graphic Designer`
  - `AI Engineer`

---

### **2. Data is Stored in Airtable**
The submission is inserted into Airtable using an **"Update/Create Record"** node.

---

### **3. Pathway Routing (Profession → Rating)**
A Pathways node checks the selected profession and routes it to the correct rating logic.

| Profession        | Rating |
|------------------|--------|
| Video Editing     | ⭐⭐⭐⭐⭐ (5 Stars) |
| Graphic Designer  | ⭐⭐⭐ (3 Stars) |
| AI Engineer       | ⭐ (1 Star) |

The rating is updated in the Airtable record automatically.

---

### **4. AI Agent Generates a Story**
The AI agent (powered by **Google Gemini Chat Model**) receives:
- Name  
- Looks  
- Profession  
- Calculated Rating  

It then generates a **personalized poem/story** based on the user’s details.

Example:
> “John, a tall and handsome AI Engineer, carried a spark of genius…“

This poem is stored under the **Poem** column in Airtable.

---

### **5. Final Airtable Update**
The workflow writes:
- Profession Rating  
- AI-Generated Poem  

…back into the same Airtable record.

---

## 📂 Workflow Visual
The workflow consists of:

1. **On Form Submission (Trigger)**
2. **Airtable – Create/Update Record**
3. **Pathways (Profession Rules)**
4. **Airtable Nodes for Each Rating**
5. **AI Agent (Gemini Model)**
6. **Final Airtable Update**

A visual reference is included in the repository for clarity.

---

## 🎥 Demo Video
A video has been included showing how the agent processes the form input and generates the final output automatically.

https://github.com/user-attachments/assets/75d27f8a-bed8-4e78-94f7-cfd58203a924

---

## 🧩 Tech Stack

| Tool | Purpose |
|------|---------|
| **n8n** | Automation workflow |
| **Airtable** | Data storage & updates |
| **Google Gemini Chat Model** | Poem/story generation |
| **Form Trigger** | Collects user input |

---

## 🏁 Features
- Fully automated end-to-end workflow  
- Auto-rating system based on profession  
- AI-generated personalized poem/story  
- Clean integration with Airtable  
- Scalable and easy to extend  

---

## 📘 Future Enhancements
- Add more professions & ratings  
- Multi-language poem support  
- Send poem to user via email/WhatsApp  
- Create an admin dashboard  

---

## 🙌 Acknowledgements
Thanks to:
- **Google Gemini AI** for powerful text generation  
- **n8n** for workflow automation  
- **Airtable** for fast and easy data handling  

