---
layout: page
permalink: /assignments_pt2/
title: Assignments_Pt2
---

* (The list will be replaced with the table of contents.)
{:toc}

***

## Assignments Submission



The data repository should include (where appropriate) :

* A REAMDE.md describing the project.
* A `requirements.txt` file listing all Python dependencies, if needed, ensuring they can be easily installed. 
* **Python 3.10** code (a notebook is fine) for demonstrating the project goals if appropriate. 

---
## Assignment 1: Texture Dataset curation

Here we will create a set of wav files of a sound "texture" that varies systematically in some dimension (Recall the water dataset "fill level"). The dataset should be 10-15 minutes of audio roughly equally distributed over the various parameter values. The data can all be in .wav (or other audio formats, see below) file (with varying parameter) or in multiple audio files. 

​	If you are generating the sounds synthetically/algorithmically, you can generate these .csv files at the same time. If you are recording, plan ahead so that the parameter files don't have to be created by hand - they can be created by processing the file (extracting the parameter, for example), or can be recorded so that the parameter values linearly from beginning to end, or is constant for the duration of the corresponding wave file,  so that the parameter file is easy to generate. 

​	In addition to the pairs of data files, there needs to be a single parameters.json file describing the parameter (see below). The complete dataset specification follows (although if you don't have different classes, and only use a single parameter of variation, it does not have to be as compex)



## **1. Required Data**

The dataset requires three types of data: **audio files**, **annotations**, and **parameter specifications**. Each one is explained below. (No installation of python code necessary!)

### **1.1 🎵 Audio Files**

Most audio file formats and sampling rates are supported, although the final model will always operate at 24kHz.

**Supported Audio Formats**: `.wav`, `.mp3`, `.flac`, `.aac`, `.ogg`, `.m4a`, `.wma`, `.aiff`, `.au`, `.ra`, `.3gp`, `.amr`, `.ac3`, `.dts`, `.ape`, `.mka`, `.opus`

### **1.2 📊 Annotations (CSV Files)**

Each audio file **must** have a corresponding CSV file with the **exact same base name**:

| Audio File  | CSV File                | Status                       |
| ----------- | ----------------------- | ---------------------------- |
| `piano.wav` | `piano.csv`             | ✅ Correct                    |
| `flute.mp3` | `flute_annotations.csv` | ⛔ Incorrect - name mismatch! |

The CSV annotation files must follow this specific structure:

- **Header row** with parameter names (must match those in `parameters.json`)
- **One row per frame** (75 frames per second)
- **Continuous parameters**: Numeric values (will be normalized to [0,1] range)
- **Categorical parameters**: Non-negative integers representing each class (0, 1, 2, ...)

Example CSV:

| saturation | reverb | instrument |
| ---------- | ------ | ---------- |
| 10.5       | 40.3   | 0          |
| 10.0       | 40.32  | 1          |
| 9.8        | 40.25  | 0          |
| ...        | ...    | ...        |

### **1.3 ⚙️ Parameter Specifications**

Information about the parameters to be controlled must be stored in a `parameters.json` file. Each parameter must specify its **name** and **type** (either `continuous` or `class`). Additional features will depepnd on the type of the parameter as follow:

**🔢 Continuous Parameters** (numeric values like tempo, volume, saturation):

- `min`/`max`: Range used for normalization
- `unit`: Physical unit (e.g., bpm, %, dB)

**🏷️ Class Parameters** (categorical values like instrument type, genre):

- `classes`: Ordered list of class names (order determines integer mapping)

#### Example `parameters.json`:

```json
{
    "parameter_1": {"name": "saturation", "type": "continuous", "unit": "dB", "min": 0,   "max": 12}, 
    "parameter_2": {"name": "reverb",     "type": "continuous", "unit": "%",  "min": 0,   "max": 100},
    "parameter_3": {"name": "instrument", "type": "class",      "classes": ["piano", "flute"]}
}
```

## **📁 2. Required File Structure**

Before running this notebook on your data, make sure it is structured as follows:

**Option 1:** Simple Structure (all data together)

```
dataset_folder/
└── raw/                         # Raw input data
    ├── parameters.json          # Parameter configuration file
    ├── piano.wav                # Audio files (various formats supported)
    ├── piano.csv                # Corresponding CSV annotations
    ├── flute.mp3                # More audio files...
    ├── flute.csv                # More CSV files...
    └── ...
```

**Option 2:** Split Structure (separate train/validation/test sets) If you want to use specific data splits for training, validation, and testing.

```
dataset_folder/
└── raw/                         # Raw input data
    ├── parameters.json          # Parameter configuration file
    ├── train/
    │   ├── piano.wav            # Training audio files
    │   ├── piano.csv            # Training CSV annotations
    │   └── ...
    ├── validation/
    │   ├── flute.mp3            # Validation audio files
    │   ├── flute.csv            # Validation CSV files
    │   └── ...
    └── test/
        ├── violin.mp3           # Test audio files
        ├── violin.csv           # Test CSV files
        └── ...
```


#### 3. Other considerations

Sound textures can be recorded or generated using any appropriate technology. Some ideas:

​	Machine sound at different speeds (preferably continuous over a range), pitched sounds (preferably continuous!), cards shuffling, spinning coins (with a parameter that goes from 0 to 1 over ), room hum, crowd "hubbub", boiling water. Chat can generate tons of "texture+parameter" ideas to help you! 

​	Textures with a single varying parameter may be difficult to find, easier to make, maybe even easier to create synthetically. Maybe some of your projects form part I of the course can generate something we could consider a "texture"?  You might also consider text-to-audio systems. 

​	***Watch out for "unwanted" variation that won't sound consistent during conditional generation!***



* OPTIONAL  : The dataset format description should be adequate for this homework. But, if you want to see how a dataset works in RNeNcodec,  you can download the "quickstart"  (watterfill) example (see the README) for that repository. (You could even trying prepping, training, and playing!)
  * Code (zipped project): https://drive.google.com/file/d/1R4GdBB9lbLVdaE4ZExBlmR03jH8ebkpV/view?usp=sharing




### Deadlines

* The assignment is due by **February 23rd** before class on GitHub Classroom (**you may work in pairs**)
* Your dataset should be sharable for others in the class and for demoing.
* Invitation to create github classroom repository for dataset assignment: (see Slack)
  

### Final Notes

---
## **Assignment 2**

### **Assignment 2a: classNN (rnencodec) training**

The dataset you created is ready for the next stage of preparation, then for training and inference. 

#### 1. 3 steps
* There are 3 notebooks in the RNeNcodec Quickstart section of the project. You just need to:
#### 1.1 📝 dataprep.ipynb -  prep the data
#### 1.2 📝 train.ipynb -  train (i suggest 75 "epochs") at first 
#### 1.3 📝inference.ipynb -  inference (interactive)

join the github classroom "classNN" for template and submission. Be prepared to share it in class!


---
### **Assignment 2b: Encodec exploration**

The dataset you created is ready for the next stage of preparation, then for training and inference. 

#### 1.1 📝Explore!
* This project repository has the "starter" Encodec utilities for moving between audio, tokens, and latents. Please push your understanding of Encodec by visualizing and listening to manipulation is the latent space. We talked about things like making a histogram of latent component values, plotting latent vector components over time (looking for correlation with sound qualities), looking at the magnitude or clustering properties of the latents, morphing between two different sounds in the Encodec latent space, generating random latents, you could try time expansion or compression in the latents space, explore what happens when cut a latent representation of sound into segments, decode each piece separately, and splice the resulting audio together (as a function of segment size), whatever it is that you are curious about or that provides a bit of scientific/creative insight. 

📁 join the github classroom "Encodec" for template and submission .Put your commented code in the notebook on the repository. Be prepared to share it in class!

### Deadlines

* The assignments are due by **March 2nd** before class on GitHub Classrooms. These are individual assignments. 

---
## **Final Assignment : Generative Audio Research Paper**
The project will involve investigation into some aspect of generative audio, largely of your choosing based on your background, scientific and musical interests, and the topics in this section of the class (below are a few suggestions). Feel free to run your ideas by me! 

### **The deliverable** 
should be in the form of a research paper, and should thus include:

* an abstract 
* background/review of related literature (2-4 papers of directed reading)
* justification of why, how, and to whom the question is interesting (new, hard, enabling)
* execution of your study (probe question with code, provide link and clear comments)
* visual and links to sonic examples
* The results of you exploration 
* Conclusion (Reflection) and future directions

The length should be roughly 1500 words (+ figures and references). ***The grade will be on clear and creative thinking, clarity of writing and presentation with visuals and audio, and generally your engagement with the issue.*** Be honest with your results. "Successful" results are not nearly as important as thinking, articulation, and learning.

### A few possible suggestions
Please choose a topic you find interesting and want to learn more about in connection with generative audio. That said, here are some ideas with a connection to the class, many based on RNeNcodec, some building on the previous assignments.  But again, you may do something the comes from a more personal interest.

* Train RNeNcodec on a couple of different sound classes, comparing results.
  * Run FAD (or similar) comparing the class separation of the datasets and the class separation of the generated sounds. Also could compare embeddings (CLAP vs VGGish)

* Study the "codebook utilization" of different audio types (music vs general audio, speech mv music, etc)

* Build a small (2-4 layer) transformer to train on a 15 minute (Encodec) data set.  
  compare to RNeNcodec, explore stacked vs flattenned codebook sequence vs latent (like RNeNcodec)  
  Explore different conditioning and/or positional encoding strategies  

* Compare RAVE latents to Encodec latents

* Implement Tokui style "style transfer" (maybe using two different codecs?). Add something new to it.

* Explore the ability of RNeNcodec to capture longer time scales with rhythms

* Extract fast-moving parameters from your audio (eg. engine sound) (spectral centroid) and use them for conditioning parameters. Generate new parameter contours for resynthesis

* Explore streaming with other codecs (Encodec 48, DAC, ...)

* Compare and analyze different training strategies in RNeNcodec (conditioning interpolation and extrapolation, drop out). 

* Compare one-hot vs continuous conditioning for discrete parameter (semitones in pitch)

* Capacity - Does the model need to be bigger to handle a bigger data set, more classes?

* (Explore "timbre transfer"  with RNeNcodec)

### Deadline

* The assignments are due by midnight Friday **March 20**. These are individual assignments, though you should feel free to discuss with your classmates. 