---
title: "Generative AI in Language Learning: User Testing Findings"
date: 2023-07-08
draft: false
description: "Key insights from three rounds of user testing for a generative AI language learning prototype, covering UI tweaks, feature evolution, and engagement strategies."
tags: ["AI Language Learning", "ICALL", "Scenario-Based Learning", "UX Design", "Findings"]
series: ["AI for Scenario-Based Learning"]
series_order: 3
---
Photo by [UX Indonesia](https://unsplash.com/@uxindo?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash) on [Unsplash](https://unsplash.com/photos/person-in-blue-long-sleeve-shirt-using-black-laptop-computer-5QiGvmyJTsc?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash)

## Introduction

When we first set out to design a [generative AI-powered language learning tool]({{% ref "/posts/1748091371063-icall-method" %}}), our goal wasn’t just to build something cool with using multiple AI modules. We wanted to create something that helps people improve at speaking a new language in a way that feels natural and maybe even a little fun.

So, we built a [prototype](https://github.com/NesR0M/AiCall_ResearchProjectSS23). We then handed it over to a group of language learners to see what worked, what didn’t, and what still needed improvement. Instead of doing one big test, we ran three iterative sessions. Why? Because learning (and designing for learning) is never a straight line. It’s messy, layered, and constantly evolving.

In each round, we listened closely to what participants said (and didn’t say), how they used the tool, where they got stuck, and what sparked their curiosity. Their feedback helped shape a better prototype and form a deeper understanding of what learners want when using AI to practice a language.

This article covers what we found along the way and what aspects of the tool needed improvements. Whether you’re an educator, a developer, or just curious about how AI can help us learn better, I hope these insights give you a window into making a digital language partner feel like it belongs in your life.

---

## Our Design Journey: Iterations Incoming!

To bring you up to speed, our testing process was split into three weekly feedback sessions, each building on the last. We brought in real German language learners to try out the prototype, share their thoughts, and help us shape it into something more useful and intuitive.

Each session followed a simple rhythm: **test**, **talk**, **improve**. Participants explored the tool and shared their experiences through interviews and creative feedback exercises. After each round, we made focused updates based on what users wanted most and what we could realistically implement in time.

This iterative setup allowed us to gather deeper insights than a one-off test ever could. By the third session, users reflected on its potential and how they could implement a similar tool in their typical setups. And that’s where the most valuable feedback came from.

### First Iteration: A Promising Start

When we launched our first testing session, we weren’t sure what to expect but were **eager** to see how learners would respond to the early version of our prototype. Thankfully, they didn’t hold back.

![First iteration of the ICALL prototype in a café scenario](first_iteration.png "First iteration of the prototype showing the café roleplay scenario with AI conversational agent and dynamic background")

Right off the bat, participants appreciated the *flexibility* in choosing different scenarios and the option to switch between typing and speaking. The **voice recording** feature, in particular, stood out. For many, it felt like a *low-pressure* way to practice speaking without worrying about making mistakes in front of others. One user even mentioned that talking to an AI felt *less intimidating* than speaking in class.

[Whisper](https://github.com/openai/whisper) (the speech-to-text engine we used) earned some unexpected praise. It often glossed over small spelling mistakes in transcriptions, which had a surprising side effect: learners felt more confident trying out **complex vocabulary** and sentence structures. When the tool didn’t penalize minor errors, they took more risks. *This is exactly the kind of learning behavior we want to encourage.*

That said, the first version of the prototype had its fair share of *rough edges*. Learners noted that the interface focused too much on text input, with little feedback or guidance to help them get started. The **robotic voice** used for text-to-speech made conversations feel *stiff* and *unnatural*. They also critiqued the visuals, which failed to *immerse* our learners.

Our testers also felt the AI was too *passive* during conversations. Too often, they were left carrying the dialogue with minimal input from the virtual partner. Their feedback was clear: the tool needed to feel more like a *real conversation* and less like typing into a form. From that first round, a few key ideas started to emerge:

1. **More dynamic AI dialogue**  
2. **Clearer onboarding and feedback**  
3. **Larger chat window**  
4. **Adjustable language complexity**  
5. **“Hover to translate”** for immediate word help

We had our work cut out for us: a solid start that proves our concept for a scenario-based ICALL app, but with a handful of *high-priority* improvements ahead.

### Second Iteration: Sharpening the Experience

Equipped with feedback from the first round, we went back to the drawing board to come up with a more **polished** version of the prototype. This second iteration was about *smoothing the rough edges* and making the experience feel more like a *real* language-learning tool, not just a tech demo.

![Second iteration of the ICALL prototype in a bakery scenario](second_iteration.png "Second iteration of the prototype showing the bakery roleplay with a refined UI: larger chat window, prominent microphone icon, and decoupled, faster image generation")

One of our first moves was to revamp the interface:

- **Bigger text output box** and a bolder microphone icon to nudge users toward the speaking mode they favored.  
- **Decoupled** dialogue output from image generation, resulting in noticeably faster response times.

Under the hood, we also replaced **[gTTS](https://pypi.org/project/gTTS/)** with **[ElevenLabs Voice AI](https://elevenlabs.io/)** for far more *natural-sounding* speech. We hesitated at first, but repeated comments on the old audio’s uncanniness convinced us this change was essential.

Next, we optimized our prompts for both **[Stable Diffusion](https://github.com/CompVis/stable-diffusion)** and **[GPT-4](https://openai.com/product/gpt-4)**. By adding a rule to center a character in each image, we gave learners a clear visual partner. And by tweaking the AI’s dialogue to be shorter and end with questions, conversations felt *more dynamic* and *human*.

We also introduced:

- **Visual language correction** for on-screen grammar and vocabulary hints  
- **Subtle audio feedback** to reinforce progress and make the tool feel truly responsive  

Although our planned translation feature was postponed, participants loved the new **conversation history panel**, and many said the language corrections made the app feel like a _real_ learning environment.

A clear theme emerged: users wanted AI responses that matched their **proficiency level**. Some found the tool too advanced, others too simple. This insight planted the seed for our next big feature: **adaptive AI responses** tuned to each learner’s skill.

The second iteration was a major leap forward. The prototype felt faster, smarter, and most importantly, more *usable*.

### Third Iteration: Forward Thinking

By the time we reached our third and final iteration, the prototype had come a long way. Aside from fixing bugs or tweaking features, this round was also about asking bigger questions: **How well does the tool support learners in the long term?** and **What should come next?**

![Third iteration of the ICALL prototype in a restaurant scenario](third_2.png "Third iteration of the prototype showing the romantic restaurant roleplay with portrait layout, click to translate feature, expanded chat area, and on-demand translation panel")


We started by refreshing the interface once again. The text output area was expanded, and we switched to a portrait-oriented image layout that placed more visual emphasis on the scenario, another step we took towards better learner immersion.

We also added a highly requested feature: **click-to-translate**! Powered by the [DeepL API](https://www.deepl.com/docs-api), this let learners translate full sentences in the chat at a single tap. While participants loved the convenience, several noted they’d actually prefer translating individual words during active practice.

Based on feedback, the new UI landed well as learners appreciated the cleaner layout, extra icons, and expanded chat space. Still, they spotted areas for polish:

- **Clearer sender distinction** between user and AI messages  
- A more **modern, app-like visual style**  
- Filling the startup screen’s white space with **conversation history**

Our scenario visuals also improved in clarity and relevance, but users craved even more engagement. Ideas included:

- **Animated avatars** or expressive feedback (e.g., changing facial expressions)  
- Deeper AI “presence” through local memory or emotional cues  

That didn’t stop them from dreaming up bold next steps:

- **Gamification features** to boost motivation  
- **Improved onboarding** for first-time users  
- **Customizable scenarios** tailored to individual goals  
- **Vocabulary suggestions** to bridge learning gaps  

This final round made one thing clear: while the core of the tool is solid, there’s a real opportunity to build something even more **personalized**, **engaging**, and **emotionally intelligent**. Thanks to our participants’ thoughtful feedback, we now have a clear roadmap for making it happen.  

---

## What Did We Learn?

Throughout all three iterations, one thing became increasingly clear: **how people interact with the tool matters as much as what the tool can do.**

### Text vs. Voice: Different Paths, Same Goal

When it came to communication style, participants naturally split into two camps:

- **Typing enthusiasts**  
- **Speaking aficionados**

Each had its strengths, but **speech-to-text (STT)** emerged as a sleeper hit. Thanks to [Whisper](https://github.com/openai/whisper), even slightly mispronounced words were transcribed accurately, giving learners a confidence boost to experiment with new vocabulary. Better inputs led to richer, more coherent outputs from [GPT-4](https://openai.com/product/gpt-4).

**The takeaway?** Giving learners flexible and forgiving ways to communicate helps lower the barrier to participation and opens up space for real growth. However, this is a **double-edged sword**, since proper communication requires proper pronunciation of words and phrases, which the tool cannot detect currently.

### Why Scenario-Based Practice Matters

Across the board, users leaned into **scenario-based learning**. They valued speaking through a scene instead of just typing, noting the record function created a **natural, low-pressure** environment.

> *“It felt less intimidating than speaking in a classroom.”*  

Without classmates to impress or teachers to interrupt, learners felt free to shape conversations. This judgment-free space translated into real confidence and motivation.

### The Limits of a Standalone Experience

Not every hurdle could be cleared. As novelty wore off, two challenges emerged:

1. **Motivation**: While some used the tool to prep for exams, many struggled to stay consistent on their own. Maybe integrating gamification techniques, like reminders, rewards, or progress tracking, could encourage regular use.

2. **AI Personality**: Learners described the chatbot as “faceless” and lacking emotional depth, memory, or character. A potential solution: add intuitive design elements, clearer guidance, or even a bit of personality (avatars, emotional cues) to make the tool feel alive.

These insights confirmed that a great AI tutor needs both **technical power** and a **human touch** to truly engage learners.  

---

## We Learned, Now What?
After three quick rounds of testing, we learned that user feedback is the fastest path from prototype to a helpful language partner. Letting learners switch between typing and speaking and framing practice as mini-scenarios made them more confident and curious. Speeding up responses, adding on-screen hints, and tuning speech quality showed that a tool’s polish matters as much as its AI core. Yet we also saw that without motivation boosters or a bit of personality, language learners quickly lost the novelty factor of the tool.

Next, we’ll turn these lessons into concrete design guidelines for **your generative AI tool**. In the next article, you’ll discover how to pick and combine *speech*, *vision*, and *language modules*, structure user flows that keep learners coming back, and sprinkle in gamification or avatars to make each session feel alive! 

> *Remember to check out the tool in our [Github](https://github.com/NesR0M/AiCall_ResearchProjectSS23)!*

**Interested in my research?** The take a look at [my other works](https://orcid.org/0000-0002-4730-7865) that cover topics ranging from using *AI in Live-Prototyping Studies* to *Affective State Change using Haptics*! 