---
layout: page
permalink: /assignments/
title: Assignments, Project and Paper Implementation
---

* (The list will be replaced with the table of contents.)
{:toc}

***

### Assignments Submission 

To submit an assignment, add your implementation to the Github Classroom Repository for each assignment.

The repository should include:

* A `requirements.txt` file listing all Python dependencies, ensuring they can be easily installed.  
* **Python 3.10** code.

### Paper Implementation

Hey AI Music Team,

We’ve got an exciting new challenge\! As you know, we’re collaborating with an avant-garde musician who’s deeply into experimenting with composition and computers. She’s looking for a real-time music generation system to play with and push the boundaries of her creative process.

I’ve found a fantastic generative music system that could be the perfect starting point. It’s called **Liquiprism**, a system that uses **cellular automata** to generate **polyrhythmic music**. I’m confident she’ll love it and find ways to expand and build on it.

You can find a detailed description in the paper: [*Liquiprism: Generating Polyrhythms With Cellular Automata*](http://www.icad.org/websiteV2.0/Conferences/ICAD2002/proceedings/36_AlanDorin.pdf).

#### Your Mission

Your task is to **re-implement Liquiprism from scratch in Python 3.10.** Keep in mind:

* Some implementation details may be missing from the paper. Don’t stress—feel free to get creative and fill in the blanks as you see fit.  
* The system described in the paper includes a visual interface, but we don’t need that for now. Focus on building a **rough prototype** to showcase to our musician collaborator.

#### Key Requirements

1. The system should function as a **real-time instrument** that pushes MIDI notes into a DAW.  
2. The DAW should have **six different instruments** for sonification, as described in the paper.  
3. Write **clean, well-documented code** to ensure we can build on it easily later.

#### Deliverables

1. **Code:**  
   * A fully functional Python implementation of Liquiprism.  
   * Ensure it’s modular and clean for future adaptations.  
2. **Demo Screencap:**  
   * Record a **2-minute screencap** of the system playing in a DAW to give an idea of how it sounds.  
   * Nothing fancy—just enough to showcase the system in action.

#### Stretch Goal (Optional)

If you’re feeling inspired, you can also:

* Implement the **visual interface** described in the paper.  
  This isn’t a requirement, but it could really impress our collaborator if you have the time and energy.

I’m sure you’ll have a great time with this implementation. If we do it right, Liquiprism could become the perfect tool for our avant-garde musician collaborator to explore new sonic frontiers.

Good luck, and as always—have fun\!

Valerio, your CTO 🎵🚀

### Assignment 1: Genetic Harmonizer Upgrade

Hey Team,

First off, great job on the genetic algorithm for harmonizing a melody\! It’s a solid first experiment, and I’m genuinely impressed with what you’ve put together so far. But, as you know, at our AI music startup, we’re all about pushing boundaries. And I think we can take this to the next level—especially with our focus on jazz harmony. Let’s make this *sing* (pun intended)\!

Our mission: **re-adapt the genetic algorithm to harmonize a melody in a jazz style.** 🎷🎼

#### Team Roles & Tasks

To tackle this challenge, I suggest we divide and conquer. Here’s what I need from you, my brilliant music AI engineers:

1. **Jazz Harmony Fitness Metrics:**  
   Develop new fitness metrics that reflect the richness and rules of jazz harmony. Think voice leading, tensions, and avoiding parallel fifths—jazz style.  
2. **Chords, Chords, Chords\!**  
   Simple triads (e.g., Cm, G) won’t cut it anymore. Expand our chord palette to include **7th chords, 9th chords, and beyond if you feel particularly fancy**. The more colorful and jazzy, the better.  
3. **Implementation & Refinement:**  
   Adapt and update the genetic algorithm implementation you worked on:  
   * Implement the new fitness metrics.  
   * Add the new chord types.  
   * Decide if the existing fitness scores stay, get modified, or are entirely replaced. This is your call—use your jazz intuition\! 🎵

Leverage your diverse skill sets\! Have the more music-savvy team members focus on crafting the jazz harmony rules, while the engineering-minded team members handle the implementation. Collaboration is key\!

#### Deliverables

Here’s what I expect at the end of this sprint:

1. **Working Code & Output:**  
   * I should be able to run your code and open the generated MIDI score in music notation software (e.g., MuseScore). I think you’ve already implemented this feature in the first iteration. So, just be sure that this works with the new implementation.  
   * The melody (let’s stick with *Twinkle Twinkle Little Star* for consistency) should be beautifully harmonized with **jazz chords.**  
2. **Documentation of Metrics:**  
   * For each fitness metric, include a short explanation directly in the code as a docstring. Keep it simple—just explain what the metric evaluates and why it’s relevant to jazz harmony.

I’m super excited to see what you’ll come up with. Feel free to experiment, get creative, and think outside the box—this is jazz, after all\! 🚀

Let’s show the world what our AI music team is capable of. Good luck\!

Valerio, your CTO

### Assignment 2: Second Order Markov Chain 

Hey Team,

I’ve reviewed your implementation of the Markov Chain melody generator, and it’s a solid start\! However, the melodies still feel a bit too random. If we’re aiming to give our music producer users a seamless and inspiring tool for creating great melodies, we need to refine this further.

Let’s stick with Markov Chains but make some important upgrades in the next sprint:

#### Proposed Changes

1. **Move to a Second-Order Markov Chain:**  
   * Update the implementation so the next note depends on the two previous ones, not just the last. This should improve coherence and make the melodies feel more intentional.  
2. **Train on the Bach Chorales Dataset:**  
   * Specifically, use the **soprano line** of the Bach Chorales for training.  
   * The dataset is available here: [Bach Chorales Dataset](https://github.com/czhuang/JSB-Chorales-dataset/tree/master).

#### Deliverables for the Sprint

1. **Data Preprocessing:**  
   * Create a Python module dedicated to preprocessing the dataset.  
   * This module should:  
     * Read the Bach Chorales dataset.  
     * Isolate the soprano line.  
     * Convert the data into a format compatible with our Markov Chain.  
     * Store the processed data in a JSON file for easy retrieval during training.  
2. **Refactored Markov Chain:**  
   * Modify the existing code to implement a second-order Markov Chain.  
3. **Main module:**  
   * When I run the main module, the code should:  
1. **Train on the Converted Dataset:**  
   * Load the processed Bach Chorales dataset stored in JSON format (make sure to include the JSON file in the repository\!).  
2. **Generate a New Melody:**  
   * By default, the model should generate a melody of **40 notes**.  
3. **Automatic Notation Display:**  
   * The generated melody should automatically open in a music notation software (e.g., MuseScore) for immediate review.

Focus on dividing the work to maximize efficiency. Some of you can handle the data preprocessing, while others refine the Markov Chain implementation. Make sure to test everything thoroughly to ensure everything’s working.

I’m excited to see how this evolves\! Good luck, and let’s make it happen. 😊

Valerio, your CTO

### Assignment 3: Rock your LSTM

Hey Team,

First off, fantastic job on the LSTM for melody generation\! I hope you learned a lot from that project. As you know, we’re pivoting to focus on chord generation instead of melody generation. I know this might feel a bit frustrating, but welcome to startup life—it’s all about adapting and seizing new opportunities. And hey, you’re going to learn a ton from this shift\!

The good news is that all the hard work you did on the LSTM for melody generation won’t go to waste. We can re-adapt it for our new mission: **coding an LSTM to automatically generate sequences of chords for rock music.**

#### The Plan

Luckily, we’ve got an amazing dataset to work with: [Rock Corpus Version 1.1](https://rockcorpus.midside.com/). This dataset includes **200 Billboard songs annotated by two experienced music theorists**. You can learn more about the dataset and the [harmonic analysis here](https://rockcorpus.midside.com/harmonic_analyses.html).

* Chords are annotated using **Roman numeral analysis** (learn more [here](https://en.wikipedia.org/wiki/Roman_numeral_analysis)).  
* Chord sequences are organized by **chorus, verse, and bridge**, giving us structure to work with.

Here’s what I suggest for the next steps:

1. **Re-adapt the LSTM Melody Generator:**  
   * Modify the model so it generates **chord sequences** instead of melodies.  
   * Train the LSTM on the **sequence of Roman numerals**, generating one Roman numeral at a time.  
2. **Redesign the Architecture (Optional):**  
   * If you think changing the LSTM architecture will improve performance (e.g., changing the number of layers / neurons), go for it\! Experimentation is encouraged.  
3. **Update the Data Preprocessors:**  
   * Adapt the data preprocessing pipeline to prepare the chord sequences from the Rock Corpus dataset in a format the LSTM can ingest.

#### Deliverables

Here’s what I expect by the end of this sprint:

1. **Training Module:**  
   * A module I can run to train the LSTM on the Rock Corpus dataset.  
   * Make sure the dataset preprocessing code is included, and document how to use it.  
2. **Generation Module:**  
   * A model I can run to generate a chord sequence, where I can specify the **number of chords** in the sequence.  
   * Output should be a simple string of Roman numerals, like this:  
     `I | ii7 | V | I`

#### Optional Stretch Goal

If you’re feeling ambitious, consider this enhancement:

* Train separate models for **verse-only** and **chorus-only** chord sequences.  
  * Verses and choruses likely have distinct chord patterns, so this could lead to more stylistically accurate results.  
  * If this feels like too much for now, it’s perfectly fine to train on all sequences at once and ignore the structural distinctions.

I’m really excited to see where this pivot takes us. The work you’re doing is laying the foundation for something truly impactful in the music tech space. Have fun with this challenge, and remember—rock on\! 🎸🎵

Valerio, your CTO

### Assignment 4: Transform my Melody

Hey Team,

I’m seriously impressed with your implementation of the Transformer architecture—wow, that’s no small feat\! 🚀

Before we dive into our ultimate goal of generating full compositions, let’s take it one step at a time. For the next phase, I suggest we focus on training the Transformer on a small, manageable dataset of melodies to test its capabilities on a more real-world problem.

#### Irish Folk Tunes Dataset

I found a dataset that’s perfect for this experiment: the [**Irishman dataset**](https://huggingface.co/datasets/sander-wood/irishman). As the name suggests, it contains a collection of Irish folk songs notated in **ABC notation**. With over 200,000 tunes available, we’ll keep things simple by using just the **first 1,000 tunes** for this experiment.

#### Your Tasks

1. **Data Preprocessing:**  
   * Create a pipeline to tokenize the **ABC notation** data, preparing it for the Transformer model.  
   * Ensure the pipeline processes input and output to handle the ABC format correctly.  
2. **Model Refactoring (if needed):**  
   * Adapt the Transformer implementation as necessary to accommodate the new music representation format.  
   * Ensure the model generates output in ABC notation.  
3. **Model Training:**  
   * Train the Transformer on the first 1,000 tunes from the Irishman dataset.  
4. **Repository Updates:**  
   * Include the subset of the dataset in the solution repository, so I can experiment with your implementation.

#### Deliverables

1. **Training Module:**  
   * A script or module that I can launch to train the model on the **1,000 Irishman tunes**.  
2. **Inference Module:**  
   * A script or module that generates a melody using the trained model, with the output in **ABC notation**.

#### Stretch Goals

These are optional, but if you have the time and want to explore further, it’d be awesome to see what you can achieve:

1. **Experiment with the Architecture and Parameters:**  
   * Tweak the Transformer’s architecture (e.g., number of layers, attention heads) or adjust training parameters (e.g., learning rate, batch size) to observe the impact on performance.  
2. **Expand the Training Dataset:**  
   * Train the model with more than 1,000 melodies—for example, try **10,000 tunes**—to see how it handles a larger dataset.  
3. **Document Your Findings:**  
   * Write a brief note summarizing your observations and results from the experiments. Include this as a **Markdown file** in the Solution folder of your repository.

I’m sure Transformers will improve our product exponentially. I have to thank you folks for the incredible job you’re doing with this. I’m really curious what’ll come up out of this new sprint. Good luck\!

Valerio, your CTO

### Assignment 5: Generative Audio Transformers

Think about something you'd like to explore and understand better about audio and transformers (the Synthformer), choose/create a dataset for addressing your questions, and explore the relationship between data, labeling, and model hyperparameters. Either technical or creative orientations are fine.

The sound quality of the results need not be great in order to explore how data and model work together. Don't worry if you don't have big compute resources and sparkling sonic results - that's not the point!

Work in groups of 1-3 people.

**Deliverables, due on our last class day, Wednesday March 5th:**

* 5 minute class presentation
* 1-1.5 page discussion of how and why you chose your dataset, how you labeled it, what question(s) you were trying to address, what you did to address your questions, and what you learned. Link to your code (start from forked [Synthformer](https://github.com/lonce/DACSynthformer))

### Final Project: Part 1 Symbolic

Hey Team,

We’ve got an exciting opportunity to showcase a **generative music tool** at an important industry conference. This is a big deal for us, and I’m counting on your creativity and skills to make it unforgettable\!

Your task is to create an **amazing generative music system** that can generate music in **semi-real-time**. What does this mean? I envision a Python program that continuously generates music, sends MIDI messages to a DAW, and uses virtual instruments or samples to sonify the output. The system should run indefinitely, generating new music on the fly.

#### The Challenge

I’m giving you total creative freedom to decide:

* **What to build:** The type of generative music system.  
* **How to build it:** The techniques and algorithms to use.

The goal is simple: create an **awesome generative AI music experience** that produces **excellent and highly creative music.**

#### Deliverables

Here’s what I need by the end of the sprint:

1. **Code Repository:**  
   * A repo containing the Python 3.10 program.  
   * Please write **clean, professional, and well-documented code**, as it will be handed over to the production team for further development if needed.  
2. **System Demo Screencap:**  
   * A **2-minute screencap** showing the system in action.  
   * I want to see how it works and get a feel for the music it generates.  
3. **System Presentation Video:**  
   * A **5-minute video** where you present and explain the system clearly.  
   * Feel free to use slides if it helps, but focus on making the explanation easy to follow.

#### Stretch Goal (Optional)

If you’re feeling ambitious, consider adding **user interaction controls** to influence the generation process. For example:

* **Motion-based Interaction:** Movement influences note density.  
* **Environmental Interaction:** Room temperature correlates with harmony dissonance.

This isn’t required, but experimenting with these ideas could make the system even more impressive. Remember, **the sky’s the limit\!**

#### Final Notes

I’m confident this project will be a lot of fun and a chance to let your creativity shine. If you deliver a killer generative music system, it will grab attention at the conference and open doors for us all.

Make sure to collaborate effectively—leverage each team member’s unique skills in music, sound design, and tech.

Good luck, and let’s make something extraordinary\!

Valerio, your CTO 🎵🚀

### Final Project: Part 2 Audio

Think of your Audio Final Project as a conference research paper.
It does not have to be "an original contribution to the literature", but can be a report on what you design as a learning project for yourself.
You may have up to a maximum of 3 co-authors (projects evaluated accordingly).

The components should include:

* A paper with a clear statement of what you set out to explore
* a literature review of relevant papers
* a description of what you did (supporting figures welcome)
* and code that comes with a ~5 minute demo (video such as a screen grab with talk-over).

Just as a few suggestions for topics (meant to inspire, not to limit):

* Explore an architecture such as the transformer input representation, architectural features, sensitivity to data, conditioning. (Train if you have the resources)

* Find trainable DDSP or RAVE models, NoiseBandNet, etc. explore parameters (eg f threshold in RAVE SVD) or module components (e.g. positional encoding)

* Exploring Alternative Tokenization Strategies for Discrete Audio Codecs (DAC) Soundstream, Encodec bit rate efficiency, evaluation strategies, streaming capabilities. Can the Descript DAC stream?

* Latent Space Interpolation and Manipulation in RAVE for Timbre Morphing

* Push the creative potential of a generative audio network

#### Deliverables

The final project deliverables are:

1. 4-5 page "conference" paper
2. A GitHub repository link containing the implementation code in the course Github Classroom.
3. A 5-minute video (like you would send to a conference) presenting your work including any demos.
