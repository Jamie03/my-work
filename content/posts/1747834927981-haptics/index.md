---
title: "Deskside Calm: Exploring AI-Driven Haptic Wellness"
date: 2024-06-24
draft: false
description: "Discover how AI-generated soundscapes and subtle haptics blend seamlessly to keep you relaxed at your desk, no screens or breaks required!"
tags: ["Haptics", "Generative AI", "Wellness", "Wearables", "UX"]
---

Photo by [Nubelson Fernandes](https://unsplash.com/@nublson?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash) on [Unsplash](https://unsplash.com/photos/woman-in-gray-sweater-covering-her-face-Cc9Yso_xn4I?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash)

## Introduction

Have you ever glanced up from your screen after hours of back-to-back video calls and realized you feel more tense than when you started? In our *hyperconnected world*, endless notifications and marathon work sessions have become the norm, and **stress** seems to tag along for the ride. As we spend more time seated, glued to laptops or phones, that mental tension only grows; the ongoing shift towards digital sedentary lifestyles has increased stress in daily life and calls for innovative approaches to improve mental and physical health.

Traditional relaxation techniques (think guided meditations, breathing apps, or quick stretch breaks) certainly help, but they often demand that you pause your workflow, switch contexts, or stare at yet another screen. In a world where multitasking rules, these methods can feel like _just one more_ item on your to-do list. This tension between our need to stay productive and our need to unwind inspired us to look beyond visual and auditory cues, and to ask: _what if you could slip into a calmer state without ever leaving your desk?_

---

## Affective Haptics Meets Generative AI

Affective haptics focuses on using touch to impact your emotional state, while advances in generative AI produce dynamic, personalized soundscapes; together, they promise seamless, multisensory experiences that gently guide users into calm states without demanding visual attention or interrupting flow.

### Turning Touch into Emotion

Affective haptics is a growing field dedicated to designing systems that can evoke or modulate emotions through tactile stimuli, from gentle pulses to complex vibration patterns. [Research on affective haptics](https://ieeexplore.ieee.org/document/7320966) has demonstrated that well-crafted haptic cues can reduce stress, enhance mood, and improve user engagement in virtual environments.

### The Rise of Generative Soundscapes

Meanwhile, generative AI has revolutionized how we create and experience audio: platforms like [Endel partner with Universal Music Group](https://pitchfork.com/news/universal-music-group-signs-deal-with-ai-startup-endel) to produce on-the-fly soundscapes tailored to factors like time of day and heart rate, helping listeners relax or focus without repetitive loops. Even artists like [Grimes](https://www.vogue.com/article/grimes-endel-ai-lullaby-sleep-soundscape) have explored AI-driven lullabies that adapt in real time to user data, showcasing the technology’s potential for personalized well-being experiences.

---

## A New Frontier: Resonant Relaxation

At its core, [Resonant Relaxation](https://zenodo.org/records/12549152) is about harnessing subtle haptic pulses and AI-generated audio to nudge you toward a calmer headspace without having to step away from your desk. Imagine a lightweight wristband or neckband that doesn’t just buzz, but _breathes_ with you, guiding your rhythm toward a more relaxed state.

![Resonant Relaxation Poster](poster.png "Resonant Relaxation: Affective State Change via Procedurally Generated Haptics")


Under the hood, our prototype is a [React](https://reactjs.org)-based web app that leans on [GPT-4o](https://openai.com/index/hello-gpt-4o/) to craft MIDI compositions from simple prompts. Those MIDI files are then turned into real-time waveforms via [Tone.js](https://tonejs.github.io) and fed into voice-coil actuators embedded in wearable patches. What you feel is two layers working in concert:

- **A breathing-paced hum**, starting just above your natural breath rate and decelerating to gently coax you into slower, deeper breathing  
- **AI-generated “sparkles”**, melodies aligned to the baseline frequency that keep the sensation novel and engaging

In our first round of user tests with three participants tackling different sedentary tasks, everyone reported feeling noticeably calmer, and most loved the textured “sparkle” layer over a plain hum.

---

## Join Us on Our Journey!

[Resonant Relaxation](https://zenodo.org/records/12549152) represents our first step toward blending AI-generated soundscapes with procedurally crafted haptic patterns right at your desk. In our paper, you’ll find a detailed walk-through of our system architecture, from the ChatGPT-driven MIDI generation to the real-time Tone.js rendering and voice-coil actuation, along with rich code snippets and visualizations. We also dive deeper into our initial qualitative study, where participants across varied sedentary tasks reported feeling _measurably more relaxed_, and unanimously loved the layered “sparkle” haptics over a simple baseline. Whether you’re a haptic designer, developer, or researcher, our open-source prototype is yours to explore and build upon on [GitHub](https://github.com/NesR0M/Resonant-Relaxation-Project).

**Interested in my research?** The take a look at [my other works](https://orcid.org/0000-0002-4730-7865) that cover topics ranging from using *AI in Live-Prototyping Studies* to *Affective State Change using Haptics*! 
