# EVAL AI: AI-Integrated Smart Interviewing System 
  
## Overview 

We have built an expert-matching system that connects candidates with suitable interviewers and provides matching scores. Building on that, the next major enhancement is to integrate a video conferencing interface and embed AI capabilities directly into the live interview process – making the entire process more intelligent, insightful, and efficient. 
 
## Key Features & Workflow 

1. Video Conferencing Integration

We will use Jitsi Meet, a free and open-source video conferencing solution, to host real-time interviews. It will be embedded directly into our platform so that candidates and interviewers can connect seamlessly.

2. Live Speech-to-Text Transcription

Each participant’s audio will be captured in real time using browser microphone access. 
These audio chunks will be sent to our backend and transcribed instantly using Whisper (OpenAI) or Google Speech-to-Text API. This gives us the full text context of the interview — who asked what, and how the candidate responded. 

3. AI-Powered Answer Evaluation & Cross-Questioning 

After each candidate response is transcribed, it is sent to an AI engine (e.g., OpenAI GPT or Grok). The AI evaluates the candidate’s answer based on relevance, depth, correctness, and clarity. It then automatically generates intelligent follow-up (cross-)questions, which are shown live to the interviewer. 

4. Real-Time AI Assistant Panel 

A small assistant window will appear next to the video call. It displays: 
•	Live transcriptions 
•	Evaluation scores (e.g., Relevance: 8.5/10) 
•	AI-suggested follow-up questions 
•	Option buttons for the interviewer to take action (Ask, Edit, Ignore) 

5. Facial Expression & Eye Movement Analysis 

To enhance the soft skill evaluation: 

•	The candidate’s facial expressions and eye movements will be analysed using computer vision tools like MediaPipe or OpenCV. 

•	The AI will assess confidence, attention, and honesty indicators, such as: 
o Eye contact consistency o Micro-expressions (nervousness, confusion) o Facial engagement (smile, frown, etc.) 

•	These insights will contribute to the behavioural analysis score. 

6. End-to-End Interview Summary & Report 

At the end of each interview, the system will generate a complete report containing: 
•	Full interview transcript 

•	AI evaluation of each answer 

•	Cross-question logs 

•	Expression and behaviour analysis 

•	Final score breakdown (technical, communication, behavioural) 

7. Intelligent Expert Scoring System

•	Combines Matching Score, Profile Score, and Relevancy Score using NLP and machine learning. 

•	Matching Score: The Matching Score measures how well an expert aligns with the interview board's subject and the candidate's expertise, based on factors like domain knowledge and relevant skills.

•	Relevancy score: The Relevancy Score predicts an expert's overall suitability for an interview, considering their Profile Score and additional factors like past interviews taken and Publications, etc.

•	Profile Score: Each expert receives a profile score based on multiple matching scores, as we need to match their skills and domain with the interview subject and candidate. 


## Tech Stack Overview 

•	Video Conferencing: Jitsi Meet 

•	Audio Transcription: Whisper / Google Speech-to-Text 


•	AI Evaluation & Question Generation: OpenAI GPT / Grok API 

•	Expression Analysis: MediaPipe / OpenCV 

•	Frontend: HTML/JavaScript / React 

•	Backend: Python (Flask or FastAPI) + SocketIO 

•	Real-Time Sync: WebSockets 

•	Database: MongoDB 

•	Hosting: Google Cloud / Render 
 
## Why This is Unique 
Unlike existing platforms such as HireVue or Interview.ai, this system supports live interviewer-candidate interaction, understands and processes responses in real time, and assists the interviewer with smart AI-generated follow-up questions. It also evaluates facial and emotional cues, offering a richer understanding of candidate behaviour. 

Our platform uses a custom NLP-based similarity algorithm to calculate a Matching Score, evaluating how well an expert’s skills align with the interview subject and candidate profile. This feeds into a Profile Score, and finally a Relevancy Score, which predicts overall expert suitability by factoring in experience, past interviews, and publications.

We implement a dynamic expert grouping strategy, selecting ideal panels from the top-matching experts, expanding the pool as needed. If internal experts aren't available, the system sources external experts using data from platforms like Google Scholar. A built-in interview scheduler automates meeting setups and keeps candidates and interviewers updated, reducing manual effort.

Moreover, it is built using cost-effective open-source tools, making it fully customizable and extensible. This makes it a truly next-generation smart interviewing platform, ideal for modern hiring workflows and scalable across industries. 
 
