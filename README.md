🤖 AI-Powered Zoom Meeting Automation using Google Calendar and n8n

🧩 About the Project
This project automates the process of scheduling Zoom meetings based on Google Calendar events using n8n and AI Agent (Gemini).  
Whenever a new event is created in Google Calendar, the AI agent analyzes it, checks whether a meeting is needed, and automatically creates a Zoom meeting if required.

It reduces manual effort and ensures all important events have a corresponding meeting ready to go.



⚙️ How It Works
1. Google Calendar Trigger: Detects when a new event is created in your Google Calendar.  
2. AI Agent (Gemini): Analyzes event details (like title or description) to decide if a meeting should be scheduled.  
3. Decision Parser: Parses AI’s output and checks if the meeting creation condition is satisfied.  
4. Zoom Integration: Automatically creates a new Zoom meeting via Zoom’s API when required.  
5. Optional: The meeting link can be emailed or stored for later use.



 🌟 Features
- 🔄 Fully automated meeting creation process  
- 🤖 AI-powered decision-making (Gemini model)  
- 📅 Real-time integration with Google Calendar  
- 📞 Automatic meeting creation in Zoom  
- 💬 Easy to customize AI prompts and logic  
- 🧠 Smart filtering of events (only creates meetings when necessary)



 🏗️ Workflow Architecture

Google Calendar Trigger 
        ↓
   AI Agent (Gemini)
        ↓
   Parse AI Decision
        ↓
Check If Meeting Needed
        ↓
    Create Zoom Meeting


 Components Explained
- Google Calendar Trigger:Starts the workflow when a new event is created.  
- AI Agent: Uses Google Gemini Chat model to interpret the event details and decide action.  
- Parser Node: Extracts decision (true/false) from AI output.  
- IF Node: Verifies if meeting creation is necessary.  
- HTTP Node (Zoom API): Sends a POST request to create a meeting automatically.

---

 🧭 Detailed Workflow Steps
1. Google Calendar Trigger Node – Detects new calendar event.  
2. AI Agent Node (Gemini Model) – Interprets event details and decides if a meeting is required.  
3.Parse AI Decision Node – Extracts true/false from AI output.  
4. IF Node – Checks condition to proceed with meeting creation.  
5. HTTP Node (Zoom API) – Creates a meeting automatically and returns the meeting link.



 🎥 Demo Example
1. Create a Google Calendar event → “Team Sync Discussion”.  
2. Workflow triggers → Gemini reads event details.  
3. Gemini decides “true” → Meeting needed.  
4. Zoom API creates meeting → Returns meeting link.  
5. Output displays meeting details.


 📧 Sample Output

Subject: Zoom Meeting Created Automatically

Hello,
A Zoom meeting has been created for your recent Google Calendar event.

Topic: Team Sync Discussion
Time: 10:00 AM - 10:30 AM
Join Link: https://zoom.us/j/123456789

Best,
Your AI Assistant




 🚀 Quick Start

 🔑 Prerequisites
- n8n (self-hosted via Docker or Cloud)  
- Google Calendar connected account  
- Zoom Developer App (JWT or OAuth credentials)  
- Gemini AI API Key  
- Basic understanding of n8n nodes



 🧰 Installation Steps
1. Open n8n and create a new workflow.  
2. Add nodes in this order:  
   - Google Calendar Trigger  
   - AI Agent (Gemini Chat Model)  
   - Function Node (Parse AI Decision)  
   - IF Node  
   - HTTP Node (Zoom Meeting Creation)  
3. Configure credentials for Google Calendar, Gemini, and Zoom API.  
4. Save and activate the workflow.



 ⚙️ Configuration

 Zoom API Setup
- Go to [Zoom App Marketplace](https://marketplace.zoom.us/)  
- Create **Server-to-Server OAuth app**  
- Copy **Client ID**, **Client Secret**, **Account ID**  
- Add them as credentials in n8n under Zoom connection.

 Google Calendar Setup
- Connect your account using n8n’s Google Calendar Trigger node.  
- Grant event read access.

 Gemini AI Setup
- Obtain an API key from [Google AI Studio](https://aistudio.google.com/).  
- Use this key inside the **AI Agent** node to enable Gemini Chat model.



 💬 AI Prompt Customization
Modify the AI prompt to change behavior.  
Example prompts:
- “Only create Zoom meetings for events with ‘meeting’ or ‘discussion’ in the title.”  
- “If event duration is more than 15 minutes, schedule a Zoom meeting.”



 🧠 Key Benefits
- Saves time by auto-creating meetings  
- Reduces manual scheduling errors  
- Adapts meeting creation intelligently using AI  
- Extensible with notifications, email, or Slack integrations







