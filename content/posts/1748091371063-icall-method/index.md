---
title: "Designing an AI-Driven Language Learning Tool"
date: 2023-07-07
draft: false
description: "Exploring how generative AI enhances scenario-based second language learning through adaptive ICALL methods and real user feedback."
tags: ["AI Language Learning", "ICALL", "Scenario-Based Learning", "Prototype", "Design"]
series: ["AI for Scenario-Based Learning"]
series_order: 2
---
Photo by [Studio Crevettes](https://unsplash.com/@louismornaud?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash) on [Unsplash](https://unsplash.com/photos/person-holding-black-pencil-on-white-printer-paper-b588L1sZHy0?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash)

## Introduction

Learning a new language is more than just memorizing vocabulary and grammar rules. It’s about connecting with people, understanding different cultures, and expressing oneself in new ways. **However, traditional language learning methods often fall short**, especially when they can’t adapt to individual learning styles or provide real-life conversational practice.

Enter Artificial Intelligence (AI). Recent advancements in AI, particularly in *Natural Language Processing (NLP)*, have opened up exciting possibilities in language education. One such innovation is **Intelligent Computer-Assisted Language Learning (ICALL)**, which uses AI to create personalized and adaptive learning experiences. These systems can analyze how learners interact with language, identify their strengths and weaknesses, and tailor lessons to fit their needs.

But we can go even further. As I covered in my [previous article]({{% ref "/posts/1748010464372-genai-icall" %}}), generative AI models can engage learners in dynamic conversations, provide instant feedback, and simulate real-world scenarios. Imagine practicing a job interview in your target language with an AI that responds naturally or exploring a virtual marketplace where you can haggle over prices from the comfort of your home.

Our research aims to bridge this gap by exploring how generative AI can create engaging, personalized, and context-rich language learning experiences. By integrating advanced AI technologies with proven language learning strategies, we hope to make language education more accessible, effective, and enjoyable for all learners.

---

## What We Set Out to Discover

When learning a new language, *one size doesn’t fit all*. People bring different experiences, personalities, and learning styles into the process, which is especially true for second language learners. So, we asked ourselves:

> *How can generative AI create personalized, scenario-based learning experiences that tap into learners’ creativity?*

Rather than just building another language app, we want to design something that adapts to the individual. We want users to understand that language learning is as much about *context and confidence* as grammar and vocabulary.

To answer this, we reviewed the current state of ICALL tools, studied their strengths, and pinpointed where they fall short in personalization and immersion. Then, we explored how modern generative AI technologies could fill those gaps.

### Designing for Real Learners

It’s one thing to imagine a smarter learning system, but another to build it in a way that truly works for people. That’s why we took a user-centered approach.

We envisioned an interconnected system of AI modules working together to create dynamic roleplay scenarios. These modules weren’t just randomly assembled, they're based on established design principles from language education research, combined with real-world input from learners.

To test our ideas, we brought in language learners from diverse backgrounds who were already on their second-language learning journeys. Our team facilitated a series of hands-on user experience (UX) sessions. These sessions weren’t just about testing the tool, they were about discovering how people interact with it, what works, what doesn’t, and how to make the experience more intuitive, engaging, and effective.

---

## Meet the Learners

We recruited five participants actively learning German as a second language. These weren’t complete beginners, but they weren’t fluent either. Their skills ranged from A1 to B1 (*beginner to lower-intermediate*). All had studied German for at least six months and were eager to improve their conversational skills. Most importantly, they represented our target users, making their feedback essential.

### How We Ran the Sessions

Instead of a single big test, we opted for an iterative approach. Over three weeks, we held three feedback sessions with all five participants. Each session lasted about an hour, giving us time to refine our prototype step by step.

- **Hands-on Testing**  
  Participants interacted with the prototype while we observed how they navigated the interface, reacted to conversations, and engaged with visual content.

- **Deep-Dive Conversations**  
  After testing, we conducted semi-structured interviews to explore their learning experiences, likes and dislikes, and improvement ideas. We focused on conversation quality, interface design, generated images, and overall usability.

We also used generative feedback methods like group brainstorming and quick sketching exercises. These helped participants clarify their ideas for features and layouts, giving us valuable insights into their vision for an ideal language-learning tool.

### Why Iteration Mattered

Each session built on the last. As learners spent more time with the tool, they offered richer feedback. This iterative format allowed us to evolve the design thoughtfully and responsively.

After each session, we reviewed the feedback and drafted changes. We prioritized updates based on:
1. **Frequency** – How often an issue was mentioned  
2. **Importance** – How crucial it seemed to participants  
3. **Feasibility** – How practical it was to implement  

This ensured our updates served the whole group and moved the project forward in a balanced way.

---

## Building the Prototype

![First iteration of the ICALL prototype in a café scenario](first_iteration.png "First iteration of the prototype showing the café roleplay scenario with AI conversational agent and dynamic background")

To support an iterative, feedback-driven design, we built a modular system with four key components:
- A simple and adaptable **user interface**  
- A tool for **converting spoken language to text**  
- A system for **realistic, AI-powered conversation**  
- An engine for **creating images based on conversation context**

These pieces had to work together seamlessly and be easy to update between sessions.

### The Tools Behind the Scenes

- [Pygame](https://www.pygame.org/): Chosen for its flexibility and ease of UI tweaks.  
- [Whisper](https://github.com/openai/whisper): For fast, multi-language speech-to-text.  
- [gTTS](https://pypi.org/project/gTTS/): For quick, cost-free text-to-speech.  
- [GPT-4](https://openai.com/product/gpt-4): Driving the conversation with human-like responses.  
- [Stable Diffusion](https://github.com/CompVis/stable-diffusion): Providing high-quality, locally-runnable image generation.

### How the Prototype Worked

1. **Start the Scenario**: The learner types or speaks their first input. Whisper transcribes speech, and GPT-4 interprets it, setting the conversation context.

2. **Generate the Visual**: A prompt combining user input and a predefined scene description is sent to Stable Diffusion, which updates the app’s background image.

3. **Interactive Loop**: 
   - Learner responds (text or speech)  
   - GPT-4 replies in the textbox  
   - gTTS reads the response aloud  
   - Stable Diffusion updates the scene if needed  

---

## What’s Next: From Prototype to Practice

With our [prototype up and running](https://github.com/NesR0M/AiCall_ResearchProjectSS23), we’ve laid the groundwork for a more personalized and immersive approach to second language learning. By integrating generative AI into scenario-based learning, we’ve opened new avenues for learners to engage with language in context-rich environments.

But building the prototype was just the beginning. The real insights emerged as we tested and refined the system with actual learners. Their experiences, challenges, and feedback have been invaluable in shaping the tool to meet their needs better.

In our next article, we’ll look into:  
- **User Feedback**: What did learners think? We’ll share their experiences and the impact on their language acquisition journey.  
- **Lessons Learned**: From successes to setbacks, we'll discuss what worked, what didn't, and how these insights can inform future developments.

> *Remember to check out the tool in our [Github](https://github.com/NesR0M/AiCall_ResearchProjectSS23)!*

**Interested in my research?** The take a look at [my other works](https://orcid.org/0000-0002-4730-7865) that cover topics ranging from using *AI in Live-Prototyping Studies* to *Affective State Change using Haptics*! 