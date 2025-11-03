# FAIO 2025 — 1st Round

🎓 **Welcome to the 1st Round of FAIO 2025!**

Dear participant, congratulations on reaching the first stage of our Olympiad!  
In this round, you'll need to solve **3 problems** covering different areas of artificial intelligence.  
Each task is worth **1 point**. The maximum score for this round is **3 points**.

# **All translations to Kazakh (Қазақша) and Russian (Русский) for the problems are in** [HERE](https://docs.google.com/document/d/1Evl7ACnQBP2_Ios0_fZS0X4fTHhgxEUpi-kimsuVPAs/edit?usp=sharing)

## Problem 1: Qaz-letters

**Task Description:**  
You need to build a machine learning model for automatic Kazakh letter classification. The dataset contains only numerical features extracted from images: statistical, geometric, projection, and transform-based features — not raw images.

**What to do:**  
Train a classification model that predicts the correct Kazakh letter based on the given features.

**Metric:**  
Performance is evaluated using Accuracy, which measures the proportion of correctly classified letters.  
The metric ranges from 0 to 1 (1 means all letters are classified correctly, 0 means none are correct).

**Task Link:**  
### **[Click here](https://www.kaggle.com/t/23291ce18385cab3fab6ff5f45f1b0ba)**

## Problem 2: Who is the best pitcher?

**Task Description:**  
Build a RAG-powered question-answering agent for Major League Baseball (MLB). The goal is to answer baseball-related questions using large, structured JSON datasets about teams, players, games, seasons, and records.

**What to do:**  
Develop a system that ingests and parses JSON data, organizes it for knowledge retrieval, and uses a retrieval-augmented generation (RAG) architecture to generate accurate answers to MLB questions.

**Metric:**  
Accuracy is the evaluation metric — the number of correct answers divided by total questions.  
The metric ranges from 0 to 1 (1 means all answers are correct, 0 means none are correct).

**Task Link:**  
### **[Click here](https://www.kaggle.com/t/96bfb8a3431c91d7479308df476fc0ee)**


## Problem 3: Misssing fundamental puzzle
**Task Description:**  
Build a pitch classification model for musical audio illusions. The goal is to identify the original musical note (e.g., C4, G#5) from audio samples in which the fundamental frequency and several harmonics have been removed.

**What to do:**  
Develop a system that analyzes mono WAV files (22050 Hz). Each file is a musical excerpt with missing frequencies—your model must reconstruct the pitch label from the spectral pattern of the remaining harmonics.

**Metric:**  
Accuracy is the evaluation metric — the number of correct predictions divided by the total number of examples.  
The metric ranges from 0 to 1 (1 means all answers are correct, 0 means none are correct).

**Task Link:**  
### **[Click here](https://www.kaggle.com/t/fbaef0197897255be8710f080fd1b4ae)**


🎉 **Good luck and enjoy the challenge!**



# FAIO 2025 — 2nd Round

🎓 **Welcome to the 2nd Round of FAIO 2025!**

Dear participant, congratulations on making it to Day 2 of our Olympiad!  
In this round, you'll face **2 new problems** that challenge your skills in computer vision and recommender systems.  
Each task is worth **1 point**. The maximum score for this round is **2 points**.

Problems in English are described below. For a quick access, check the right side (see **"Table of Contents"**). For a Kazakh or Russian translation please click **[HERE](https://docs.google.com/document/d/1lLR4P-DFDZ2fQxSNLfa_EFoIsO5DNoHtjWnbgy4z3J0/edit?usp=sharing)**

## Problem 1: Personalized Music Recommender
**Task Description:**  
Given real-world listening data from the hitter and Izi music apps, your task is to build a system that recommends the **top 50 most relevant tracks** for each user, based on their preferences and listening history.

**What to do:**  
- Develop a model that predicts which songs each user will enjoy most—and how much they’ll actually listen.
- You can use classical ML, deep learning, or hybrid approaches—any strategy to produce high-quality recommendations.

**Metric:**  
- For each test user, recommend exactly 50 tracks ranked by predicted relevance.
- Score: For each recommendation, record the fraction of the track listened (from 0.0 to 1.0); sum and average these values to compute the final normalized score (0.0 to 1.0).

**Task Link:**  
### **[Click here](https://www.kaggle.com/t/8298025698a57213001f0536bfaa21ee)**

## Problem 2: Lost in the Museum
**Task Description:**  
Can your AI recognize a masterpiece—even when the photo is blurry, tilted, or half-cropped?  
You are given 20,000 images, including 10,000 high-quality gallery shots of paintings, 1,000 real-world “query” photos (blurred, cropped, poorly lit), and 9,000 distractors.  
Your objective is to generate **feature embeddings** for all images so that, even with drastic appearance changes, each real-world photo can be matched robustly to its correct painting in the gallery using **cross-domain image retrieval**.

**What to do:**  
- Build a system that encodes each image (pixels only, no metadata) into a fixed-size feature vector.
- Ensure that each “query” photo is close to its genuine gallery painting in the embedding space, and far from distractors.

**Metric:**  
The competition uses the **Hit@3** metric:
- For every query photo, if the correct gallery painting appears in the **top 3 most similar images** (via cosine similarity of embeddings), it’s counted as a hit.
- Final score: the fraction of query images with a correct match in the top-3 list (ranges from 0.0 to 1.0).

**Task Link:**  
### **[Click here](https://www.kaggle.com/t/1a1226a3500cc1d0fb182a42f60c4d41)**

🎉 **Good luck and enjoy the challenge!**
