---
title: "On-the-Fly AI Prototyping: Revolutionizing UX Testing"
date: 2025-05-14
draft: false
description: "We propose the AI-of-Oz framework for live prototyping using generative AI that transforms typical usability tests into dynamic, co-creative workshops."
tags: ["User-Centered Design", "Generative AI", "Live Prototyping", "UX Testing", "HCI"]
---
Photo by [Amélie Mourichon](https://unsplash.com/@amayli?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash) on [Unsplash](https://unsplash.com/photos/person-writing-on-white-paper-MKDEMlPRoYU?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash)

## Introduction

Picture this: you’re conducting a typical usability test on a new piece of software, watching a participant click through the polished interface you just designed. You’ve poured hours into wireframes, mockups, and scenario scripts, but as soon as they hit **“send,”** the feedback rolls in: _“I wish these labels were clearer,”_ _“Can this answer more naturally?”_ Now you’re back at your desk, juggling design sprints and waiting for the next round of user tests. It’s a familiar rhythm in **user-centered design (UCD)**, but it can feel more like a marathon than a conversation.

Traditional UCD methods champion this iterative process: gather user needs, build a prototype, test, tweak, and repeat. While tools like [Figma](https://www.figma.com/) make it easy to spin up high-fidelity screens, real change often waits until “after the study” when code catches up to ideas. By then, those “aha” moments from participants risk fading into meeting notes or getting lost in the backlog.

**What if we could cut that lag down to zero?** What if you could tweak the component your user is touching, right as they’re touching it? That’s the core of our research question: _“How can generative AI be used to enable live-prototyping within user studies?”_ Instead of a human “Wizard-of-Oz” manually swapping screens, what about using generative artificial intelligence (AI) to tweak features and elements of the prototype?

To bring this vision to life, we propose a conceptual framework for using generative AI to facilitate live-prototyping. We then conducted a case study with prototyping experts using our framework to run a live session. We gathered their responses to see if this idea is viable in a real-world setting.

---

## Where Today’s Frameworks Fall Short

Even with all the buzz around AI-powered design tools, there’s still a stubborn lag between hearing what users want and seeing those ideas live in a prototype. Let’s walk through where today’s approaches speed things up—and where they stall out.

### Narrow AI-Prototyping Plugins

- [PromptInfuser](https://dl.acm.org/doi/10.1145/3544549.3585628) lets you bind UI mock-ups in [Figma](https://www.figma.com/) to LLM prompts, so text inputs spin back AI-generated responses on the same screen. Designers loved catching prompt mismatches early; however, you still have to polish every change by hand, and you’re limited to text fields, not full interfaces.
- **Text-to-Image Generators** like [Stable Diffusion](https://github.com/CompVis/stable-diffusion) and [Midjourney](https://www.midjourney.com/) produce style ideas or rough mockups, serving as a “catalyst for brainstorming” rather than final assets. Designers must translate those images into usable UI components, and you can’t tweak them live in a user session.
- **AI-Assisted Feedback Analysis** tools can cluster and summarize user comments after a study, cutting down transcription and coding drudgery. But this still happens _after_ the prototype has been shipped for testing, so design updates remain an offline affair.

### Big-Picture AI-UCD Frameworks

- [DesignFusion](doi.org/10.1115/1.4065487) decomposes design tasks into subcomponents and uses multi-model reasoning to generate concept art, with a mixed-initiative toolkit for designer intervention. It streamlines ideation, but stops short of swapping components during a live test.
- [AI-UCD](https://publications.eai.eu/index.php/casa/article/view/4211) embeds AI across nine UCD steps, from user research through ethical auditing and validation. It ensures rigorous, data-driven iterations, yet still follows a sequential cycle: _test → analyze → refine_. There’s no mechanism for in-session tweaks.

### Classic (and AI-Augmented) Wizard-of-Oz

- Traditional [Wizard-of-Oz experiment](https://www.semanticscholar.org/paper/Wizard-of-Oz-Prototyping%3A-When-and-How-Bernsen-Dybkjaer/45522a09bebc352de3e27ae1c61bb3bf66f7b681) uses human “wizards” hidden behind the scenes to fake unbuilt features. It captures real user–system interactions, but operators juggle hotkeys, face fatigue, and introduce inconsistency, which limits scalability.
- [Apprentice of Oz](https://ieeexplore.ieee.org/document/8673205) automates subtasks to ease the wizard’s burden, boosting reliability. However, designers still rely on a human-in-the-loop, and it wasn’t designed for rapid, multi-model component swaps on the fly.

Frameworks like DesignFusion and AI-UCD leverage generative AI to dynamically support ideation and enable multi-model reasoning to build iterative feedback loops. Yet in both cases, prototype changes still wait for “after the test.” What if you didn’t have to? Imagine using a quick prompt to tweak the prototype’s behavior while your participant is still in session. This in-the-moment agility could collapse testing and iteration into one fluid conversation, revealing deeper insights and transforming every usability study into a co-creative exploration.

---

## Introducing the AI-of-Oz Framework

Imagine you’re in the middle of a usability session and your participant pauses, frowns at the screen, and says,  
> *“Could this button look more playful?”*  

Instead of jotting down a note and promising to revisit it later, you flip over to your hidden control panel, tweak a simple prompt:

> _“Make the button rounder and add a subtle bounce animation.”_

and hit **update**. In seconds, the prototype on your user’s screen shifts to match that request, letting you see in real time whether that playful bounce resonates.

![AI-of-Oz live-prototyping framework diagram](ai-diagram.jpg "Participants interact with the prototype while designers update AI components live using a separate control interface.")

At the core of this approach is **live-prototyping**: constructing your interface out of generative AI components that can be created, swapped, or reshaped on demand. As sketched in the figure above, every feature your participant interacts with is driven by one or more AI models—GPT powering conversational bits, Stable Diffusion crafting on-the-fly imagery, or other specialized engines for charts, layouts, and even voice. Behind the scenes, you work in a second interface that participants never see. Here, you type clear text prompts for your language model or adjust parameters in a diffusion dashboard, instantly regenerating whatever element needs tweaking.

Because the user only ever sees a polished front end, you can experiment freely:

- **Need a completely new illustration?** Chain two models together: let one generate background art and feed it into an LLM to produce contextual captions.
- **Want to A/B test button labels, dialog tones, or color schemes?** Switch them mid-session and watch which variant sparks that “aha” moment.

This method isn’t just about speed; it’s about collapsing the traditional _test, then iterate later_ cycle into one fluid exchange. Every piece of feedback becomes an invitation to co-create, and every adjustment deepens your understanding of what truly works. By embedding generative AI directly into your prototyping toolkit, you turn every user study into a live design lab, where ideas evolve on the spot and insights emerge organically.

---

## Conclusion & Next Steps

By integrating generative AI directly into your user sessions, you can transform every study into a live workshop. But as you picture this in your workflow, you might ask yourself:

- *How would a live prototyping session look?*
- *How can I design my prototype with the framework in mind?*

In our paper, we tested our framework in action by flipping the script: we had prototyping experts improve a language-learning prototype that adheres to our framework’s principles. We then simulated typical user feedback and observed how experts addressed the requests.

Curious to see these live-prototyping sessions decoded? Head over to [“The AI of Oz”](https://www.mdpi.com/2076-3417/15/10/5506) to check out our framework diagram, user reflections on what worked (and what didn’t), and the next-generation toolkit we’re building to make in-session design both practical and inspiring.

**Interested in my research?** The take a look at [my other works](https://orcid.org/0000-0002-4730-7865) that cover topics ranging from using *AI in Live-Prototyping Studies* to *Affective State Change using Haptics*! 