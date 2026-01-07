---
layout: page
permalink: /assignments/
title: Assignments
---

* (The list will be replaced with the table of contents.)
{:toc}

***

## Assignments Submission 

To submit an assignment, add your implementation to the Github Classroom Repository for each assignment.

The repository should include:

* A `requirements.txt` file listing all Python dependencies, ensuring they can be easily installed.  
* **Python 3.10** code.

---
## Assignment 1: Genetic Jazz Melody Generator

Hey Team,

Great work on the previous genetic algorithm assignment — you’ve already proven that you can make evolutionary systems *behave musically*. Now it’s time to raise the bar and step fully into jazz territory. 🎷

This time, we flip the problem.

Instead of harmonizing a melody, your system will generate a melody that fits a given jazz chord progression.

### Mission

Design and implement a genetic algorithm that generates a melodic line over a predefined 8-bar jazz chord progression, under the following constraints:

* 8 bars, 4/4
* 1 chord per bar
* All chords are 7th chords (e.g. maj7, min7, dom7, half-diminished, etc.)
* The chord progression is given and fixed
* The melody must be stylistically and harmonically compatible with the progression

Think lead sheet *jazz melody*, not classical counterpoint.

### High-Level Goal

Your task is to evolve melodies that:
* Outline the underlying harmony
* Use musically meaningful chord tones and tensions
* Exhibit good melodic motion and phrasing
* Sound plausible as a jazz melody (even if simple)

### Team Roles & Tasks

As before, I strongly recommend splitting responsibilities.

#### 1. Jazz-Aware Fitness Metrics

Design fitness functions that evaluate how well a melody fits a jazz chord progression.

Examples (you don’t need to implement any of these):

* Emphasis on chord tones on strong beats
* Controlled use of tensions (9ths, 11ths, 13ths)
* Penalization of “wrong” notes against the chord
* Stepwise melodic motion vs. excessive leaps
* Motivic consistency across bars
* Phrase-level contour (e.g. avoiding randomness)

Each metric should reflect a musical intuition.

#### 2. Melody Representation
Decide how a melody is encoded genetically. For example:
* Notes per bar
* Pitch + duration genes
* Fixed rhythmic grid vs. evolving rhythm

Keep it simple but meaningful.

#### 3. Genetic Algorithm Design

Adapt the GA from the previous implementation to this new task.

You are free to:
* Keep parts of the old fitness
* Modify them
* Remove them entirely

Justify your choices musically and technically.

### Chord Progression
You may:

* Use a provided jazz progression (e.g. ii–V–I variants), or
* Define your own 8-bar progression, as long as:
  * It contains only 7th chords
  * 1 chord per bar
  * It is clearly documented in the code

The system should be able to receive a chord progression with the characteristics above as input.

The chord progression must remain fixed during evolution.

### Deliverables
#### 1. Working Code & MIDI Output 
* The code must run end-to-end
* The system must generate:
  * A melody
  * Over the given chord progression
* Export the result as a MIDI file
* The MIDI should be readable in notation software (e.g. MuseScore)

#### 2. Fitness Metric Documentation
For each fitness metric, include:

* A short docstring explaining:
  * What it evaluates
  * Why it matters musically (in a jazz context)

#### 3. Presentation

Depending on the number of teams, you may be asked to present your work in class
* 5-minute presentation (prepare slides)
  * What have you done?
  * How? 
* Be ready with a MIDI rendering, and a score of one of the outputs of your system. We’ll try to play the output in class with live musicians. If not, we’ll fall back to the MIDI.

### Deadlines
* The assignment is due by **February 15th** at midnight on GitHub Classroom
* Your team will (possibly) present on February 16th in class

### Final Notes

This assignment is deliberately open-ended.

There is no single “correct” jazz melody — what matters is whether:

* Your system encodes musical reasoning
* Your fitness functions make aesthetic sense
* The results improve over generations

Experiment, listen critically, and trust your musical intuition.

Let’s see if your algorithms can swing. 😉

Good luck!

Your CTO, Valerio

--- 

## Assignment 2: Polyphonic Transformer for Bach Chorales

Hey Team,

You’ve already shown that you can work with Transformer architectures. In this assignment, you’ll take the next step and apply them to a classic benchmark task in symbolic music generation: polyphonic modeling of Bach chorales.

### Mission
Train a polyphonic Transformer model on the Bach chorales dataset, capable of generating coherent multi-voice musical textures.

You may:
* Adapt the starter implementation provided, or
* Adapt any other Transformer-based implementation you consider appropriate

The focus is on understanding the modeling choices, not on re-implementing everything from scratch.

### Tasks

#### 1. Data Handling
* Use the [full Bach chorales dataset](https://www.kaggle.com/datasets/pranjalsriv/bach-chorales-2)
* Choose an appropriate symbolic representation (e.g. piano-roll, event-based, token-based)
* Clearly document your representation choice

#### 2. Model Training
* Train a Transformer-based model for polyphonic music generation
* Justify key design choices (representation, sequence structure, conditioning, etc.)

#### 3. Inference
* Generate new chorale-like samples
* Export results as MIDI files for listening and inspection
* Export results in MuseScore or other notation software, in a nice score that can be easily sight-read. Consider using [music21](https://www.music21.org/music21docs/) for this.

### Deliverables
#### 1. Code
* Training script/module
* Inference script/module to generate new samples
* Generated MIDI examples
* A short README or Markdown note describing:
  * Representation
  * Model architecture
  * Any deviations from the starter implementation

#### 2. Presentation
Depending on the number of teams, you may be asked to present your work in class
* 5-minute presentation (prepare slides)
  * What have you done?
  * How? 
* Be ready with a MIDI rendering, and a score of one of the outputs of your system. We’ll try to play the output in class with live musicians. If not, we’ll fall back to the MIDI.

### Reference Paper (Suggested)

You are encouraged to read at least the following paper:

- [Music Transformer: Generating Music with Long-Term Structure](https://arxiv.org/pdf/1809.04281)

(You don’t need to reproduce this system. Use it as a conceptual reference.)

### Deadlines

- The assignment is due by **February 15th** at midnight on GitHub Classroom
- Your team will (possibly) present on February 16th in class

Looking forward to hearing your machines channel their inner Johann Sebastian. 😉

Valerio, your CTO

---

## Final Project

Hey Team,

We’ve got an exciting opportunity to showcase a **generative music tool** at an important industry conference. This is a big deal for us, and I’m counting on your creativity and skills to make it unforgettable!

Your task is to create an **amazing generative music system** that can generate music in **semi-real-time**. What does this mean? I envision a Python program that continuously generates music, sends MIDI messages to a DAW, and uses virtual instruments or samples to sonify the output. The system should run indefinitely, generating new music on the fly.

### The Challenge
I’m giving you total creative freedom to decide:

* **What to build**: The type of generative music system.
* **How to build it**: The techniques and algorithms to use.

The goal is simple: create an **awesome generative AI music experience** that produces excellent and highly creative music.

Feel also free to use pre-trained Hugging Face models if you want.

### Deliverables
Here’s what I need by the end of the sprint:

* **1. Code Repository:**
  * A repo containing the Python 3.10 program on GitHub Classroom
  * Please write clean, professional, and well-documented code, as it will be handed over to the production team for further development if needed.

* **2. 10-minute Presentation (live):**
  * Explain the system clearly (focus on making the explanation easy to follow)
  * Show the system in action
  * I want to see how it works and get a feel for the music it generates

### Stretch Goal (Optional)

If you’re feeling ambitious, consider adding user **interaction controls** to influence the generation process. For example:

* **Motion-based Interaction**: Movement influences note density.
* **Environmental Interaction**: Room temperature correlates with harmony dissonance.

This isn’t required, but experimenting with these ideas could make the system even more impressive. Remember, the sky’s the limit!

### Deadlines

The final project is due by **February 16th** at midnight on GitHub Classroom
Your team will present on February 17th in class

### Final Notes
I’m confident this project will be a lot of fun and a chance to let your creativity shine. If you deliver a killer generative music system, it will grab attention at the conference and open doors for us all.

Make sure to collaborate effectively—leverage each team member’s unique skills in music, sound design, and tech.

Good luck, and let’s make something extraordinary!

Valerio, your CTO 🎵🚀

---
