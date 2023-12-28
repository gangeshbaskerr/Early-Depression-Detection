![Early Mental Depression Detection System](https://github.com/gangeshbaskerr/Early-Depression-Detection/assets/130077430/7120b6f7-6cfc-4cf8-9a74-132d750c691f)
    ![made-with-jupyter-notebook](https://user-images.githubusercontent.com/130077430/230479936-93dbcbd0-275b-4af7-9231-cceeb91d8a84.svg)          ![migrated-to-oneapi](https://user-images.githubusercontent.com/130077430/230487901-cbcdf13f-1d36-477d-9a7c-1917fa579da9.svg)![built-by-team-geeks](https://user-images.githubusercontent.com/130077430/230486285-e9e8fdbc-4579-4d0e-a448-550b423199b2.svg)
<img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/gangeshbaskerr/DriverDrowsinessDetection-OneAPI"> <img alt="GitHub watchers" src="https://img.shields.io/github/watchers/gangeshbaskerr/DriverDrowsinessDetection-OneAPI?style=social">
<hr/>

# Inspiration  <img src="https://user-images.githubusercontent.com/130077430/230579469-c1263cef-784e-4845-93fb-2f73544e49e1.png" width="90" height="80"> 
In the contemporary landscape, the urgency for an accurate and accessible method to detect depression has never been more apparent. As society contends with increasing stressors, a growing segment of the population grapples with depressive tendencies. Recognizing the need for early intervention, our research is motivated by the imperative to develop a model that autonomously detects depression. We propose leveraging three essential modalities derived from clinical interviews to validate our model: physiological, speech, and visual cues.
Extensive research underscores the intricate signs of depression, which are best captured through the simultaneous study of these three modalities. Changes in mental behaviour during depression are reflected in physiological and speech alterations, including stammering, uneven pauses, and altered pronunciation. The video modality adds a behavioural dimension, capturing abnormal eye contact, reduced mouth movement, and changed posture. Integrating lexical analysis provides valuable context, enriching our understanding of the subject's mental state.

<img src="https://github.com/gangeshbaskerr/Early-Depression-Detection/assets/130077430/c7ae1004-e532-4ed9-99d1-521d2df7b737" width="330" height="280"><img src="https://github.com/gangeshbaskerr/Early-Depression-Detection/assets/130077430/1b3799eb-fe1a-476a-96f9-515d3f87de87" width="330" height="280"><img src="https://github.com/gangeshbaskerr/Early-Depression-Detection/assets/130077430/803e426a-bcc8-4a7a-8f83-b5a3bf0d68cc" width="330" height="280">

<hr/>

# Problem Statement <img src="https://user-images.githubusercontent.com/130077430/230730194-a7389fed-f5fd-48d3-856a-0212057f2500.png" width="90" height="80">

Depression whispers in many voices, often beyond the reach of words alone. It murmurs in speech hesitations,
the fleeting shadows on a face, and the veiled emotions embedded in language. Traditional methods, relying
solely on self-reported symptoms, are deaf to these whispers, leaving millions shrouded in silent suffering.
**OUR CHALLENGE **:
to build a model that becomes a skilled translator, deciphering the multifaceted language of depression. We
need to weave together a tapestry of audio, video, and text, listening to what's said, how it's said, and what the
body reveals. This tapestry, more prosperous and more nuanced, will paint a more accurate picture of a
person’s mental state, revealing depression's hidden secrets before they take root.
But this quest demands overcoming **formidable obstacles**. 

**1. Orchestrate the cacophony of data:**
Aligning audio, video, and text in perfect harmony to capture the intricate correlations that whisper hidden truths. 

**2. Amplify the faintest signals:**
differentiating the subtle tremors in speech, the fleeting glances on video, And the veiled emotions within words from the background
noise. 

**3. Personalize the diagnosis:**
crafting a model that adapts to the unique language of depression in each individual, transcending a one-size Fits all approach.


<hr/>

# Introduction <img src="https://user-images.githubusercontent.com/72274851/152814876-73362bcc-bde6-411f-ba80-235e911f276f.gif" width="90" height="90">

In today's fast-paced world, the shadow of depression looms large. Recognizing its presence before it 
casts deeper darkness is crucial, yet relying solely on self-reported symptoms might miss the intricate 
whispers it leaves behind. Our project embarks on a journey to unveil depression's secrets, not just 
through what individuals say but by listening to the symphony of signals their bodies whisper – in their 
voices, expressions, and words.

Conventionally depression detection was done through extensive clinical interviews, wherein the subject’s responses 
are studied by the psychologist to determine his/her mental state. In our model, we try to imbibe this approach by fusing 
the 3 modalities i.e. word context, audio, and video and predict an output regarding the mental health of the patient. 
The output is divided into different levels to take into consideration the level of depression of the subject. We’ve 
built a deep learning model that fuses these 3 modalities, assigning them appropriate weights, and thus gives an output.

This isn't just about identifying depression; it's about understanding its intricate language, unlocking a 
door to earlier intervention and more effective treatment. By listening to the whispers of the body and 
the echoes of the mind, we hope to paint a brighter future for those struggling in the shadows, where 
early detection becomes the first step towards reclaiming the light.
 

<hr/>

# Approach <img src="https://cdn0.iconfinder.com/data/icons/data-science-2-1/66/119-512.png" width="90" height="80"> 

**SYSTEM OVERVIEW**

In my proposed system for depression detection, we initiate the process by extracting features from audio, visual, and textual modalities. These features are integrated based on timestamps, emphasizing their time-dependent interactions. The pre-processing stage involves aligning features at a sentence level to capture contextual nuances between words.

**GATING MECHANISM AND FEATURE CONTROL**

Following feature extraction, a crucial step involves applying a gating mechanism to regulate the influence of different modalities on the final output. Weight vectors are introduced for each modality, enabling the system to learn and control the transformation of information carried forward. At each time step, feature vectors from each modality are concatenated and passed through a word-level LSTM (Long Short-Term Memory) equipped with the gating mechanism. Before concatenation, audio and visual vectors undergo additional gating mechanisms to extract 
essential information.

**HYBRID FUSION FOR ENHANCED PERFORMANCE**

An alternative approach incorporates a hybrid fusion technique, strategically combining early and late fusion benefits. This can occur at one or two levels, with feature fusion initially creating a new modality. This newly formed modality is then treated as an additional individual modality, and its scores or decisions are fused with those of the original modalities. This hybrid fusion strategy aims to optimize information integration for improved model performance in 
depression detection.

<hr/>

# Procedure <img src="https://th.bing.com/th/id/R.02832177b40b49d50674126476f980c3?rik=aXibwvpQe645bg&riu=http%3a%2f%2fwww.clipartbest.com%2fcliparts%2fjcx%2f6rb%2fjcx6rbngi.png&ehk=xllVkMLnEE%2fEXx%2fnWbpceiVVfvTNGJmODcZ9fEBJVGA%3d&risl=&pid=ImgRaw&r=0" width="120" height="100"> 

## 1️⃣ Pre-install all the required libraries
       1) nltk
       2) numpy
       3) pandas
       4) gensim
       5) gc
       6) keras
       7) smart_open
       8) sklearn
       9) matplotlib
      10) tensorflow 
## 2️⃣ Understand the dataset
  The Dataset was never downloaded locally due to its large size and other computational limitations.The code snippets in Dataset.ipynb were used to obtain from the           DAIC server, unzip them and arrange them in a manner we saw fit for easy implementation. The DAIC-WOZ dataset, curated by the University of Southern California, is a        subset of the broader DAIC (Distress Analysis Interview Corpus) aimed at aiding the diagnosis of psychological distress conditions, including anxiety, depression,           and PTSD. Comprising clinical interviews, the Dataset features audio and video recordings and extensive questionnaire responses. The Wizard-Of-Oz interviews,                conducted by an animated virtual assistant named Ellie, are also included, where a human interviewer controls Ellie in a separate room. The data is meticulously             transcribed and annotated, encompassing verbal and non-verbal features.
 
## 3️⃣ Data preprocessing

  **VIDEO MODALITY** :
  The Dataset incorporates 388 features extracted from facial expressions, including 68 2D and 68 3D facial points, 24 AU features measuring facial activity, 16 features 
  for gaze representation, and 10 features for pose representation.

  **AUDIO MODALITY** :
  In the audio modality, features are sampled at 100Hz, offering insights every 10ms. Encompassing 12 Melfrequency cepstral coefficients (MFCCs), pitch tracking features,    and parameters like F0, VUV, NAQ, QOQ, H1H2, PSP, MDQ, peakSlope, Rd, Rdconf, MCEP0-24, HMPDM0-24, and HMPDD0-12, theaudio features are comprehensive.

  **TEXT MODALITY** :
  The textual modality consists of a conversation transcript in CSV format, timestamped at the sentence level and classified by the speaker. Expressions like laughter are     annotated, and the Dataset comprises 189 sessions, varying from 7 to 33 minutes, featuring interviews with 59 depressed and 130 non-depressed subjects.

## 4️⃣ Build and train the model
The audio and video features are first passed through 3 feedforward highway layers. Then, dense layers are used to reduce the dimensionality of both video and text features. After concatenation, LSTM with 128 hidden nodes is used. Finally, a dense layer is applied with sigmoid activation to get the output. A learning rate of 0.0001 is used. An EarlyStopping callback is used from Keras API for the number of epochs. The audio and video features are first passed through 3 feedforward highway layers. Then, dense layers are used to reduce the dimensionality of both video and text features. After concatenation, (Bi)LSTM with 128 hidden nodes is used. Finally, a dense layer is applied with sigmoid activation to get the output. A learning rate of 0.0001 is used. For the number of epochs, the EarlyStopping callback is used from Keras API.

<img src="https://github.com/gangeshbaskerr/Early-Depression-Detection/assets/130077430/a2ca5635-041a-4e31-b52e-18d7ca41cccd" width="650" height="500">  <img src="https://github.com/gangeshbaskerr/Early-Depression-Detection/assets/130077430/1a719889-4830-44fe-a337-837eb4c50930" width="340" height="500">

## 5️⃣ Train the model using Intel OneAPI to get better results

<img src="https://user-images.githubusercontent.com/72274851/218504609-585bcebe-5101-4477-bdd2-3a1ba13a64a8.png" width="190" height="100"><img src="https://aditech.in/wp-content/uploads/2020/07/image_2020_07_17T06_08_48_297Z.png" width="800" height="100">

**How does OneApi provide better performance :**
    
Today’s computer systems are heterogeneous and include CPUs, GPUs, FPGAs, and other accelerators. The different architectures exhibit varied                   characteristics that can be matched to specific workloads for the best performance.
Having multiple types of compute architectures leads to different programming and optimization needs. oneAPI and SYCL provide a programming model, whether through direct programming or libraries, that can be utilized to develop software tailored to each of the architectures.
    
**Advantages of using OneAPI :**

1) We can use Single code for both CPU and GPU (heterogeneous computing)
2) To implement machine learning based IoT projects easily with less hardwares as the machine learning part happens in cloud
3) To process files faster ie. it takes less time to run the epochs
4) OneAPI allows users to transcend Hardware restrictions and provide better performance for low powered computers
5) Accuracy will improve while using OneAPI

<img src="https://user-images.githubusercontent.com/130077430/230733185-94fbda70-6fe6-40af-985c-d7f8a74a3521.jpg" width="495" height="400"><img src="https://user-images.githubusercontent.com/130077430/230733189-78e03097-7c88-4f42-9c0e-159e58aa7972.jpg" width="495" height="400">

To migrate your project to OneAPI : 
[click here!](https://devcloud.intel.com/oneapi/get_started/) to get started

For reference : [click here!](https://www.youtube.com/watch?v=NkJXCalgmeU)
    
    
## 6️⃣ Save the model
       save the model to calculate the accuracy and loss
    
<hr/>

# Accuracy and Loss      <img src="https://user-images.githubusercontent.com/130077430/230577475-9af43d03-1a50-41c2-99b2-e1a28b69c84e.png" width="90" height="80">

<img src="https://github.com/gangeshbaskerr/Early-Depression-Detection/assets/130077430/3815d123-3e32-4e77-b119-713ce21ab237" width="495" height="500"> <img src="https://github.com/gangeshbaskerr/Early-Depression-Detection/assets/130077430/d328ab5a-f8a5-4415-b578-b1a8462af56d" width="495" height="500"> 

<hr/>

# Conclusion <img src="https://user-images.githubusercontent.com/130077430/230730394-3dfbc977-435b-4a6f-bfa3-fc193606f0e0.png" width="90" height="80">

In conclusion, our presented model offers a robust approach to detecting depression by leveraging audio, video, and lexical indicators. By implementing a sentence-level model with highway layers as a gating mechanism, our results indicate that this approach outperforms alternative models. Incorporating a hybrid fusion technique, combining early and late fusion, enhances the interpretability of each modality, contributing to the overall effectiveness of our model.There is potential for further refinement in feature extraction, focusing on additional audio parameters such as response time, pauses, and silence rate. Exploring the interaction between bodily action sequences from motion capture data and verbal behaviour could provide a more comprehensive understanding of depressive symptoms. Our model lays the foundation for future advancements, suggesting avenues for in-depth exploration and improvement in depression detection methodologies.

<hr/>
