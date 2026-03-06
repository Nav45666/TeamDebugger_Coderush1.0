<h1 align="center">TeamDebugger – CodeRush 1.0 Hackathon Project</h1>

<p align="center">
A web-based healthcare assistance platform developed during the <b>CodeRush 1.0 Hackathon</b>.
The system integrates machine learning, interactive tools, and a conversational chatbot
to provide preliminary health insights and improve user accessibility to healthcare analysis tools.
</p>

<hr>

<h2>Overview</h2>

<p>
This project was developed as part of the CodeRush 1.0 Hackathon. The goal was to design
a platform capable of assisting users with preliminary health insights using a combination
of machine learning models, medical data analysis tools, and interactive interfaces.
</p>

<p>
The platform combines several healthcare-oriented tools including disease prediction,
medical report analysis, and AI-assisted interaction through a chatbot system.
One of the core research components of the project involved developing a machine learning
pipeline to detect schizophrenia using EEG signals.
</p>

<hr>

<h2>My Contributions</h2>

<p>
I contributed to several key parts of the project including machine learning development,
chatbot implementation, and front-end integration.
</p>

<ul>
<li>Designed and trained a machine learning model for schizophrenia detection using EEG data.</li>
<li>Developed the chatbot interface and integrated it with an external API.</li>
<li>Implemented the conversational logic for the chatbot to assist users navigating the platform.</li>
<li>Developed the homepage interface and helped integrate core system components.</li>
<li>Integrated the machine learning pipeline with the platform's workflow.</li>
</ul>

<hr>

<h2>Machine Learning Model – Schizophrenia Detection using EEG</h2>

<p>
One of the primary research components of the project involved developing a deep learning
pipeline capable of identifying schizophrenia-related patterns in EEG signals.
</p>

<p>
Schizophrenia diagnosis traditionally relies on behavioral observations and clinical
evaluations. EEG signals capture electrical activity in the brain and can reveal
neurophysiological patterns that may indicate neurological disorders.
</p>

<p>
The goal of the model was to analyze EEG recordings and classify whether a subject
shows patterns consistent with schizophrenia or belongs to a healthy control group.
</p>

<hr>

<h3>Dataset</h3>

<p>
The EEG data used for this project was obtained from publicly available datasets
hosted on Kaggle. These datasets contain EEG recordings from both healthy individuals
and individuals diagnosed with schizophrenia.
</p>

<p>
EEG signals are recorded using electrodes placed on the scalp following the
international <b>10–20 electrode placement system</b>. Each electrode records
electrical activity from different regions of the brain over time.
</p>

<p>
The EEG data was represented as multidimensional arrays in the following format:
</p>

<pre>
(trials, channels, time_samples)
</pre>

<ul>
<li><b>Trials</b> – Individual EEG recordings</li>
<li><b>Channels</b> – Electrodes capturing activity from different brain regions</li>
<li><b>Time Samples</b> – Sequential voltage measurements over time</li>
</ul>

<p>
Example structure used during development:
</p>

<ul>
<li>20 EEG trials</li>
<li>19 EEG channels</li>
<li>1000 time samples per trial</li>
</ul>

<hr>

<h3>Signal Preprocessing</h3>

<p>
EEG signals are highly sensitive to noise and artifacts caused by eye movements,
muscle activity, and electrical interference. Before feeding the signals into the
deep learning model, preprocessing steps were applied to improve signal quality.
</p>

<ul>
<li>Bandpass filtering to remove low-frequency drift and high-frequency noise</li>
<li>Removal of power-line interference using notch filtering</li>
<li>Artifact reduction for eye movement and muscle noise</li>
<li>Segmentation of EEG recordings into fixed-length windows</li>
<li>Normalization of signal amplitudes</li>
</ul>

<p>
These preprocessing steps ensure that the model focuses on meaningful neural
patterns rather than noise.
</p>

<hr>

<h3>Feature Extraction</h3>

<p>
To capture both temporal and frequency-domain information from EEG signals,
multiple signal processing techniques were used.
</p>

<ul>
<li>Wavelet Transform for time–frequency analysis</li>
<li>Fourier Transform for spectral frequency analysis</li>
<li>Band power estimation across EEG frequency bands</li>
</ul>

<p>
These features allow the model to detect abnormal oscillatory brain activity
patterns associated with schizophrenia.
</p>

<hr>

<h3>Deep Learning Architecture</h3>

<p>
The model used for EEG classification was based on the <b>EEGNetv4 architecture</b>,
a convolutional neural network specifically designed for EEG signal processing.
</p>

<p>
EEGNet is widely used in brain-computer interface research due to its efficiency
and ability to extract both spatial and temporal patterns from multichannel EEG data.
</p>

<p>
The architecture consists of several specialized layers:
</p>

<ul>
<li><b>Temporal Convolution Layers</b> – Capture temporal patterns in EEG signals</li>
<li><b>Depthwise Convolution Layers</b> – Learn spatial relationships between electrodes</li>
<li><b>Separable Convolution Layers</b> – Reduce computational cost while maintaining performance</li>
<li><b>Batch Normalization</b> – Stabilize neural network training</li>
<li><b>Dropout Layers</b> – Prevent model overfitting</li>
<li><b>Fully Connected Layer</b> – Produce the final classification output</li>
</ul>

<p>
The model processes EEG signals and outputs probability scores representing
whether the EEG pattern corresponds to a healthy subject or a subject
showing schizophrenia-related neural patterns.
</p>

<hr>

<h3>Machine Learning Pipeline</h3>

<pre>
EEG Dataset (Kaggle)
        ↓
Signal Cleaning and Preprocessing
        ↓
Segmentation into Time Windows
        ↓
Feature Extraction (Wavelet + Fourier)
        ↓
Tensor Conversion
        ↓
EEGNetv4 Deep Learning Model
        ↓
Binary Classification
        ↓
Schizophrenia Detection
</pre>

<hr>

<h2>Chatbot System</h2>

<p>
In addition to the machine learning model, I developed the chatbot system
integrated within the healthcare platform.
</p>

<p>
The chatbot was designed to provide users with an interactive interface
that assists them in navigating the platform's healthcare tools and
understanding available features.
</p>

<h3>Chatbot Features</h3>

<ul>
<li>Interactive conversational interface</li>
<li>Integration with external APIs for response generation</li>
<li>Real-time user interaction within the web interface</li>
<li>Guidance for navigating healthcare tools on the platform</li>
</ul>

<hr>

<h2>Additional Platform Features</h2>

<p>
Alongside the EEG-based schizophrenia detection system and chatbot interface,
the platform includes additional health analysis tools developed by the team.
</p>

<ul>
<li>Blood report analysis</li>
<li>Symptom-based disease prediction</li>
<li>Image-based disease scanning</li>
</ul>

<p>
Together, these features create a unified healthcare assistance platform
designed to provide preliminary health insights.
</p>

<hr>

<h2>Technologies Used</h2>

<ul>
<li>Python</li>
<li>PyTorch</li>
<li>Braindecode</li>
<li>NumPy</li>
<li>Pandas</li>
<li>HTML</li>
<li>CSS</li>
<li>JavaScript</li>
<li>External APIs(gemini-2.0-flash)</li>
<li>Visual Studio Code</li>
</ul>

<hr>

<h2>Hackathon Context</h2>

<p>
This project was developed under the time constraints of the CodeRush 1.0
Hackathon. The focus was on rapid prototyping, collaborative development,
and building functional components within a limited timeframe.
</p>

<p>
The project demonstrates the integration of machine learning,
biomedical signal processing, and web technologies to create
an interactive healthcare assistance platform.
</p>
