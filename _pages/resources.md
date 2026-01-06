---
layout: page
permalink: /resources/
title: Resources
---

* (The list will be replaced with the table of contents.)
{:toc}

***

## Learning Material (Part 1)

### Required

#### Generative Music AI Theory \+ Implementation

* The Sound of AI’s *Generative Music AI Course*:  
  * [Video lectures (theory \+ implementations)](https://www.youtube.com/watch?v=NpJWprrqlFw&list=PL-wATfeyAMNqAPjwGT3ikEz3gMo23pl-D)  
  * [Code \+ slides](https://github.com/musikalkemist/generativemusicaicourse/tree/main)  
* Theory behind RNNs/LSTMs as covered in the following videos of the *Deep Learning (for Audio) with Python*:  
  * [Recurrent Neural Networks Explained Easily](https://www.youtube.com/watch?v=DY82Goknf0s)  
  * [Long Short Term Memory (LSTM) Networks Explained Easily](https://www.youtube.com/watch?v=eCvz-kB4yko)  
* The Sound of AI’s *Generating Melodies with LSTM Nets Course*:  
  * [Video lectures (theory \+ implementation)](https://www.youtube.com/watch?v=FLr0r-QhqH0&list=PL-wATfeyAMNr0KMutwtbeDCmpwvtul-Xz)  
  * [Code \+ slides](https://github.com/musikalkemist/generating-melodies-with-rnn-lstm/tree/master)

#### Generative Music AI Papers

* [GenJam: A genetic algorithm for generating jazz solos](https://www.researchgate.net/publication/2342018_GenJam_A_Genetic_Algorithm_for_Generating_Jazz_Solos)  
* [The Generative Electronic Dance Music Algorithmic System (GEDMAS)](https://www.academia.edu/101959323/The_Generative_Electronic_Dance_Music_Algorithmic_System_GEDMAS_)  
* [Liquiprism: Generating Polyrhythms With Cellular Automata](http://www.icad.org/websiteV2.0/Conferences/ICAD2002/proceedings/36_AlanDorin.pdf)  
* Automatic Stylistic Composition of Bach Chorales with Deep LSTM (aka BachBot) \[[presentation](https://www.youtube.com/watch?v=yu3DZuxxV7c)\] \[[paper](https://archives.ismir.net/ismir2017/paper/000156.pdf)\]  
* Museformer: Transformer with Fine- and Coarse-Grained Attention for Music Generation \[[paper](https://proceedings.neurips.cc/paper_files/paper/2022/file/092c2d45005ea2db40fc24c470663416-Paper-Conference.pdf)\]\[[website](https://ai-muzic.github.io/museformer/)\]
* Music Transformer: Generating Music with Long-Term Structure \[[blog](https://magenta.tensorflow.org/music-transformer)\] \[[paper](https://arxiv.org/pdf/1809.04281)\]

#### Symbolic Music Representation Formats

* \[TODO\] Course Doc and implementation for MIDI and abc notation   
* Basic MIDI tokenizations such as [MIDI-Like](https://miditok.readthedocs.io/en/latest/tokenizations.html#midi-like) from MIDITok

### Optional (but suggested, for real\!)

#### Deep Learning

* The Sound of AI’s *Deep Learning (for Audio) with Python*:  
  * [Video lectures (theory \+ implementation)](https://www.youtube.com/watch?v=fMqL5vckiU0&list=PL-wATfeyAMNrtbkCNsLcpoAyBBRJZVlnf)  
  * [Code \+ slides](https://github.com/musikalkemist/DeepLearningForAudioWithPython/tree/master)

#### Clean Code

* The Sound of AI’s  *Uncle Bob’ SOLID Principles for Machine Learning Engineers Course:*  
  * [Video lectures (theory \+ implementation)](https://www.youtube.com/watch?v=ul8LLiFY0Dw&list=PL-wATfeyAMNpZ6-ESiXK9BnZmGLjqECt9)  
  * [Code \+ slides](https://github.com/musikalkemist/solidforml/tree/main/solidforml)  
* [Clean Code in Python \- Second Edition: Develop maintainable and efficient code](https://www.amazon.es/Clean-Code-Python-maintainable-efficient/dp/1800560214)


## Learning Material (Part 2)

### Papers on Generative Audio 

* Van Den Oord, A., Dieleman, S., Zen, H., Simonyan, K., Vinyals, O., Graves, A., ... & Kavukcuoglu, K. (**2016**). **Wavenet**: A generative model for raw audio. *arXiv preprint arXiv:1609.03499*, *12*.

* Kumar, K., Kumar, R., De Boissiere, T., Gestin, L., Teoh, W. Z., Sotelo, J., ... & Courville, A. C. (**2019**). **Melgan**: Generative adversarial networks for conditional waveform synthesis. *Advances in neural information processing systems*, *32*.
​		[keywords: Vocoder; Phase construction]

* Engel, J., Agrawal, K. K., Chen, S., Gulrajani, I., Donahue, C., & Roberts, A. **(2019**). **Gansynth**: Adversarial neural audio synthesis. *arXiv preprint arXiv:1902.08710*.
​		[keywords: conditional training]

* Engel, J., Hantrakul, L., Gu, C., & Roberts, A. (**2020**). **DDSP**: Differentiable digital signal processing. *arXiv preprint arXiv:2001.04643*.
​		[keywords: inductive bias, signal processing units, real time]

* Caillon, A., & Esling, P. (**2021**). **RAVE**: A variational autoencoder for fast and high-quality neural audio synthesis. *arXiv preprint arXiv:2111.05011*.
​		[keywords: conditional training]

* Huzaifah, M., & Wyse, L. (2021). Deep generative models for musical audio synthesis. *Handbook of artificial intelligence for music: foundations, advanced approaches, and developments for creativity*, 639-678.
​		[keywords: "review" paper]

* Wyse, L., Kamath, P., & Gupta, C. (2022, April). Sound model factory: An integrated system architecture for generative audio modelling. In *International Conference on Computational Intelligence in Music, Sound, Art and Design (Part of EvoStar)* (pp. 308-322). Cham: Springer International Publishing.
​		[keywords: playability; latent space]

* Garcia, H. F., Seetharaman, P., Kumar, R., & Pardo, B. (2023). Vampnet: Music generation via masked acoustic token modeling. *arXiv preprint arXiv:2307.04686*.
​		[keywords: transformer, in-painting, masking for training, codecs]
  
* Evans, Z., Parker, J. D., Carr, C. J., Zukowski, Z., Taylor, J., & Pons, J. (**2024**). **Stable audio open**. *arXiv preprint arXiv:2407.14358*.
​		[keywords: Text-2-audio; Open (data, weights, code, latent diffusion]

* Rafael Valle, Rohan Badlani, Zhifeng Kong, Sang-gil Lee, Arushi Goel, Sungwon Kim, Joao Felipe Santos, Shuqi Dai, Siddharth Gururani, Aya AlJa’fari, Alex Liu, Kevin Shih, ˜ Wei Ping, Bryan Catanzaro (**2024**). **Fugatto** 1 Foundational Generative Audio Transformer Opus 1
