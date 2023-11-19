# Auto-Tuning-using-Python
INTRODUCTION
Problem Statement: 
Singing in tune is indeed a crucial skill for singers, and it can be challenging for some individuals. Hence, we are going to implement auto-tuning using python coding and DSP (Digital Signal Processing).
Solution:
Pitch correction or Auto-tuning
1.	Pitch tracking – Detect the pitch of the voice at the given point of time. There are various algorithms for pitch tracking, such as the YIN algorithm, autocorrelation, and frequency-domain methods. These algorithms analyse the frequency content of the audio signal to estimate the pitch at different points in time.
2.	Planning – Making a strategy to adjust the actual pitch to the desired pitch to make the vocals in tune. Machine learning models can be trained to learn the mapping between detected pitch and desired pitch based on a dataset of correctly tuned examples.
3.	Pitch shifting – Adjusting the recorded vocals to the desired pitch. Implementing the strategy used in the previous step and making adjustments in the pitch to match the desired pitch.
These steps collectively are known as auto-tune.


UNDERSTANDING THE PROJECT

What is Auto-tune? 
Auto-Tune is a pitch correction software and technology designed to correct or manipulate the intonation (pitch) of a singer's vocal performance. It was developed to address pitch inaccuracies in vocal recordings. Auto-Tune automatically detects the pitch of a vocal performance and adjusts it to the nearest correct pitch. This corrects off-key notes and helps create a smoother and more polished sound.

 

For a straightforward command-line auto-tune tool, Python is the preferred choice due to the extensive availability of Digital Signal Processing (DSP) algorithms as Python packages. Leveraging these packages, such as LibROSA and PyDub, ensures efficient implementation of pitch detection and correction functionalities. Whether it's pitch tracking, algorithmic adjustments, or real-time processing, Python's robust capabilities make it well-suited for creating a functional and efficient auto-tune tool that can be easily integrated into various audio processing workflows.

Key features and aspects of Auto-Tune:
1.	Pitch Correction:
Auto-Tune automatically detects the pitch of a vocal performance and adjusts it to the nearest correct pitch. This corrects off-key notes and helps create a smoother and more polished sound.
2.	Real-Time Processing:
Auto-Tune can be applied in real-time, allowing for immediate correction during live performances or recording sessions. This has made it a valuable tool for both studio production and live events.
3.	Graphical User Interface (GUI):
Many versions of Auto-Tune come with a graphical user interface that displays the pitch curve of the vocal performance. This allows producers and engineers to visually identify and edit pitch corrections.
4.	Artistic Effect:
While originally designed for corrective purposes, Auto-Tune's unique sound has been embraced as an artistic effect. The exaggerated pitch correction, especially when set to extreme levels, can create a robotic or synthetic vocal sound that has been popularized in certain genres of music.
5.	Versions and Settings:
Auto-Tune software often comes in different versions, and users can adjust various settings to control the speed of pitch correction, the extent of correction applied, and other parameters.
6.	Popularity in Music Genres:
Auto-Tune gained significant popularity in the late 1990s and early 2000s, particularly in the hip-hop and pop genres. Artists like T-Pain and Kanye West played a role in popularizing the use of Auto-Tune as a deliberate stylistic choice.
7.	Controversy:
The use of Auto-Tune has been a subject of debate in the music industry. Some argue that it enhances the creative possibilities for artists, while others criticize it for contributing to a homogenized and overproduced sound.
It's important to note that while Auto-Tune is widely recognized for its corrective capabilities, its use as a stylistic effect has become a distinctive element in contemporary music. Many artists intentionally incorporate Auto-Tune to achieve a specific sound or to experiment with vocal textures in their music.

Applications of auto-tune:
Auto-tune applications are software tools designed to correct or manipulate the pitch of vocal performances in real-time or during post-production. These applications use digital signal processing (DSP) algorithms to adjust the intonation of a singer's voice. Auto-tune has become widely popular in the music industry for its ability to create a polished and tuned vocal sound. Here are some notable auto-tune applications:
1.	Antares Auto-Tune:
Antares Auto-Tune is one of the most well-known and widely used auto-tune plugins. It's available in various versions, including Auto-Tune Pro, Auto-Tune Artist, and Auto-Tune Access. It provides both automatic and manual pitch correction features.
2.	Celemony Melodyne:
Melodyne is a versatile pitch correction tool that goes beyond traditional auto-tuning. It allows for precise pitch and time manipulation of individual notes within a recorded audio file, providing more detailed control over the correction process.
3.	Waves Tune:
Waves Tune is a real-time pitch correction plugin that offers intuitive controls and flexible pitch correction options. It is commonly used in both studio and live settings.
4.	Celemony Auto-Tune Access:
Celemony, known for Melodyne, also offers Auto-Tune Access, a more streamlined and user-friendly version of pitch correction software. It is designed for quick and easy pitch correction tasks.
5.	MAutoPitch (MeldaProduction):
MAutoPitch is a free and simple auto-tune plugin provided by MeldaProduction. It includes basic pitch correction features and is suitable for users on a budget.
6.	Logic Pro Flex Pitch:
Logic Pro, Apple's digital audio workstation, includes Flex Pitch, a built-in pitch correction tool. It allows users to edit the pitch of audio recordings directly within the DAW.
7.	FL Studio NewTone:
FL Studio includes NewTone, a pitch correction and time manipulation tool. It enables users to correct and adjust the pitch of vocal recordings within the FL Studio environment.
8.	Pro Tools Elastic Audio:
Avid's Pro Tools includes Elastic Audio, a feature that enables users to manipulate pitch and time in recorded audio. It provides various algorithms for pitch correction and time-stretching.
9.	iZotope Nectar:
iZotope Nectar is a vocal processing plugin that includes pitch correction capabilities. It is known for its comprehensive set of tools for vocal production, including EQ, compression, and harmonization.

LITERATURE REVIEW
1.	Pitch Tracking: For pitch detection, we are using PYIN algorithm which is an improved version of the YIN (Pitch detection algorithm based on the YIN paper by Alain de Cheveigné and Hideki Kawahara) algorithm and was introduced by A. Mauch and S. Dixon in their paper "PYIN: A Fundamental Frequency Estimator Using Probabilistic YIN
PYIN Algorithm:
The PYIN algorithm, or Pitch YIN, is a pitch detection algorithm designed for monophonic (single-note) audio signals. It's an improved version of the YIN (Pitch detection algorithm based on the YIN paper by Alain de Cheveigné and Hideki Kawahara) algorithm and was introduced by A. Mauch and S. Dixon in their paper "PYIN: A Fundamental Frequency Estimator Using Probabilistic YIN." The primary goal of PYIN is to accurately estimate the fundamental frequency (pitch) of a musical note in an audio signal.

Key points about the PYIN algorithm:
i.	Probabilistic Approach:
PYIN introduces a probabilistic approach to pitch detection. It estimates the probability distribution of pitch candidates, providing a more robust and accurate pitch estimation, especially in the presence of noise.
ii.	Pitch Estimation:
The algorithm aims to estimate the fundamental frequency of a musical note in a given audio signal. This is crucial for tasks such as music transcription and analysis.
iii.	Harmonic Structure:
PYIN considers the harmonic structure of the audio signal to improve pitch detection. It uses a pitch candidate tracking mechanism that takes into account the harmonics of the fundamental frequency.
iv.	Thresholding and Confidence Measures:
PYIN uses a thresholding mechanism to determine the presence of pitch candidates. Additionally, it provides confidence measures associated with the estimated pitch, allowing users to assess the reliability of the results.
v.	Python Implementation:
There are Python implementations of the PYIN algorithm available in various libraries. For example, the librosa library, which is commonly used for music and audio analysis in Python, includes a PYIN pitch detection algorithm.
The pyin function is available in the LibROSA library for pitch estimation using the Probabilistic YIN (PYIN) algorithm. This function is part of LibROSA's pitch module, and it aims to provide a more accurate estimation of the fundamental frequency (pitch) in monophonic audio signals.




2.	Pitch Adjustment Strategy: 
•	Mapping to Musical Score: One approach is to use a reference musical score to determine the desired pitch at different points in the recording. This can involve comparing the detected pitch with the expected pitch from the score.
•	Manual Adjustment or Predefined Scales: In some cases, a simple manual adjustment might be sufficient. Alternatively, predefined scales or user-defined preferences can be used to guide the pitch correction process.
•	Machine Learning: Machine learning models can be trained to learn the mapping between detected pitch and desired pitch based on a dataset of correctly tuned examples.

3.	Pitch Shifting: For pitch shifting, we are using PSOLA algorithm, that stands for Pitch-Synchronous Overlap-and-Add.

PSOLA algorithm:
PSOLA (Pitch Synchronous Overlap and Add) is a time-domain algorithm commonly used for pitch shifting and time-stretching of audio signals. The primary goal of PSOLA is to modify the pitch of a signal without changing its duration. This algorithm is particularly useful for applications such as voice modification, pitch correction, and musical effects.

Key principles of the PSOLA algorithm:
i.	Pitch Synchronous Processing:
PSOLA operates in a pitch-synchronous manner. It identifies the pitch period of the input signal and processes the signal in overlapping windows that align with the pitch periods.
ii.	Overlap and Add:
The algorithm divides the input signal into frames, each centred around a pitch period. Overlapping windows are applied to these frames, and the pitch period is adjusted by stretching or compressing the frames. The modified frames are then overlapped and added together to produce the final output.
iii.	Pitch Detection:
PSOLA requires an accurate pitch detection mechanism to identify the pitch period of the input signal. Various pitch detection algorithms, such as autocorrelation or YIN, can be used in conjunction with PSOLA.


iv.	Time-Stretching and Pitch Shifting:
PSOLA allows for independent control of time-stretching and pitch-shifting factors. Adjusting the overlap between frames and the pitch period determines the degree of modification applied to the input signal.
v.	Artifact Reduction:
To minimize artifacts introduced by pitch modification, PSOLA often includes additional signal processing steps, such as windowing and amplitude modification. These steps help to smooth transitions between frames and reduce audible artifacts.
vi.	Real-Time and Offline Processing:
PSOLA can be implemented for real-time processing, making it suitable for applications like voice synthesis during live performances. It can also be used in an offline mode for processing pre-recorded audio.
vii.	Implementation in Various Programming Environments:
PSOLA has been implemented in various programming environments and languages, including MATLAB, Python, and C++. Implementing PSOLA typically involves a combination of pitch detection algorithms and signal processing techniques.

A combination of an OLA-technique with resampling allows us to change the pitch of a signal without changing its duration. OLA is used to counteract the inherent time-scale modification outcome of the resampling part.
Implementing PSOLA (Pitch Synchronous Overlap and Add) in Python involves several steps, including pitch detection, frame processing, and overlap-and-add operations. Here is a simplified example using Python. Note that this is a basic illustration, and you may need to refine and optimize the code for specific use cases.

METHODOLOGY
1. Parse command line arguments:
   a. Specify the input vocals file.
   b. Optionally, set the plot flag to visualize the results.
   c. Choose the correction method: 'closest' or 'scale'.
   d. If the correction method is 'scale', specify the musical scale.


2. Load the audio file:
   a. Use librosa to load the audio file with specified sample rate (sr).
   b. If the file is stereo, use only the first channel.

3. Choose the correction function:
   a. If the correction method is 'closest', use the closest_pitch function.
   b. If the correction method is 'scale', use aclosest_pitch_from_scale with the specified                scale.

4. Perform pitch tracking using PYIN algorithm:
   a. Set frame length, hop length, and frequency range.
   b. Use librosa.pyin to estimate pitch (f0), voiced flag, and voiced probabilities.

5. Apply the chosen correction strategy to the pitch:
   a. Use the correction function on the pitch values obtained from PYIN.
   b. Optionally, perform median filtering for additional smoothing.

6. If plotting is enabled, visualize the results:
   a. Generate a spectrogram of the audio.
   b. Overlay the original pitch trajectory and the corrected pitch trajectory.

7. Perform pitch-shifting using the PSOLA algorithm:
   a. Use psola.vocode with the original audio, corrected pitch, and specified frequency range.

8. Write the corrected audio to an output file:
   a. Specify the output file path based on the original file name.
   b. Use soundfile (sf) to write the corrected audio.


9. Execute the script:
   a. Run the main function when the script is executed.

10. To run the script from the command line:
    a. Provide the vocals file path.
    b. Optionally, specify the correction method ('closest' or 'scale') and the musical scale.
    c. Use the '--plot' flag to enable visualization of the results.




FUTURE EXPANSION 
The potential future expansions to enhance this auto-tuning audio project are:
1.	Improved Pitch Detection Algorithms:
•	Explore and integrate more advanced pitch detection algorithms or enhancements to the existing PYIN algorithm. This can contribute to more accurate pitch estimation, especially in challenging audio environments.
2.	Multi-Vocal Harmonization:
•	Extend the project to support multi-vocal harmonization. Implement algorithms that analyze and adjust the pitch of multiple vocal tracks to create harmonies, providing a richer musical experience.
3.	Customizable Correction Profiles:
•	Introduce a feature that allows users to create and customize correction profiles. Users can define specific pitch correction behaviors, adjusting parameters such as correction strength, scale adherence, and artifact reduction to match their artistic preferences.
4.	Real-Time Visualization and Control:
•	Develop a real-time visualization component that displays the pitch correction applied to the input audio. Additionally, provide real-time control over correction parameters, allowing users to interactively adjust the pitch correction during playback or live performances.
5.	Integration with Music Theory:
•	Incorporate music theory principles to enhance the auto-tuning process. Implement features such as intelligent chord detection, suggesting pitch corrections that align with the underlying harmony, or providing options for users to choose specific musical modes for correction.

These expansions aim to not only improve the accuracy and functionality of the auto-tuning tool but also introduce new capabilities that cater to a wider range of musical scenarios and user preferences. User customization, real-time interaction, and support for harmonization can significantly broaden the project's utility.

CONCLUSION

To sum up, the Python-based autotuning project has proven to be a highly effective solution for optimizing system performance. Leveraging advanced algorithms and machine learning, the project dynamically adjusts parameters, offering a more efficient alternative to manual tuning. Beyond efficiency gains, it contributes to resource optimization, energy efficiency, and system stability. Its adaptability makes it applicable across diverse domains, and being open-source, it fosters collaboration and ongoing development. In essence, the project signifies a significant step toward automating system configuration, showcasing the potential of computational techniques for achieving superior performance in the evolving technology landscape.



REFERENCES
[1] M. Mauch and S. Dixon, pYIN: A Fundamental Frequency Estimator Using Probabilistic Threshold Distributions, in Proceedings of the IEEE International Conference on Acoustics, Speech, and Signal Processing (ICASSP 2014), 2014.

[2] De Cheveigné, Alain, and Hideki Kawahara, YIN, a fundamental frequency estimator for speech and music, The Journal of the Acoustical Society of America 111.4 (2002): 1917-1930. 

[3] E. Moulines and F. Charpentier, Pitch-synchronous waveform processing techniques for text-to-speech synthesis using diphones, Speech communication, 1990. 
