# 🧠 Conversational AI Assistant (Google Ecosystem-Powered)
This project is a Conversational AI Assistant built entirely on Google's ecosystem of APIs, delivering a seamless voice-based user experience. It combines natural speech recognition, intelligent language understanding, and voice response — all accessible via an intuitive Gradio interface. Demo Video link: ```https://youtu.be/RHRuy1XxFa4```, ```https://youtu.be/AeYzyF7Ne18```,```https://youtu.be/53fxm90F9Gc```


## 1. Google Speech-to-Text API
Captures and transcribes real-time microphone input using Google’s high-accuracy STT (Speech-to-Text) engine — ensuring fast and robust voice command recognition.

## 2. Google Gemini 2.5 Flash
Empowered by the Gemini 2.5 Flash model, this assistant intelligently processes user prompts to:
1. Generate natural conversations
2. Interpret intent
3. Make context-aware decisions
4. Interface with third-party APIs when needed

## 3. Google Text-to-Speech (GenAI SDK)
Converts Gemini’s generated responses into human-like speech using Google’s Text-to-Speech GenAI SDK — enabling a smooth conversational flow via spoken feedback.

## 4. Google Calendar API Integration
Integrated with the user’s Google Calendar, this assistant can:
1. Fetch and read out upcoming events
2. Create new calendar events via natural language commands

## 5. Gradio UI Wrapper
All components are beautifully packaged within a Gradio-based web interface, allowing users to:
1. Interact with the assistant via microphone and speaker
2. Visualize waveform outputs
3. Manually control actions like start, stop, and send

# 🚀 Installation

## 1. Clone this repository
```git clone https://github.com/saurabhkumar9901/GeminiConversationalAI```
## 2. Install Miniconda
In Windows Command prompt
These three commands quickly and quietly download the latest 64-bit Windows installer, rename it to a shorter file name, perform a silent install, and then delete the installer:
```
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe -o .\miniconda.exe
start /wait "" .\miniconda.exe /S
del .\miniconda.exe
```
## 3. Creating Virtual environment 
```
conda create --name env python=3.10.14
conda activate env
pip install -r requirements.txt
```
## 4. Execute
Open assignment.ipynb in VS-code:
```
Cntrl+Shift+P to select the interpretor and choose the environment. Your newly created env name should appear there.
```
# 📘 NOTE
1. Make sure to generate the API key via this link
   ```https://aistudio.google.com/apikey```
2. Go to the ```https://console.cloud.google.com/``` and enable:
   1. Google Calender API (Check quickstart guide at ```https://developers.google.com/workspace/calendar/api/quickstart/python``` for setting up the API for authentication)
   2. Google Speech-to-Text
   3. Make sure to enable these above API's for the same project you are using in the Google cloud console
3. Create a ```.env``` file in the working/project directory with the following ```GOOGLE_API_KEY= your-aistudio-google-com-key-here```
  
# N8N and ReTell AI
1. Make your free account on ```https://www.retellai.com``` and ```https://n8n.io/```
2. Go to n8n.io login and create a workspace after creating the workspace import the import_me_in_n8n.json file in this GitHub repository
3. Copy the Webhook trigger production URL in the clipboard
4. Go to retellai.com and create an agent
5. Under Functions tab add the details as following:
   1. API endpoint: Select method POST and enter the Webhook trigger production URL
   2. Parameters: Select Form and give name "prompt" and under description "user's message" and select required.
   3. Check the box Speak after execution
6. Execute your workflow in n8n
7. Click test agent in retellai
