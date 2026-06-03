[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.nm000346-blue)](https://doi.org/10.82901/nemar.nm000346)

CastillosCVEP100
================

c-VEP and Burst-VEP dataset from Castillos et al. (2023)

Dataset Overview
----------------
  Code: CastillosCVEP100
  Paradigm: cvep
  DOI: https://doi.org/10.1016/j.neuroimage.2023.120446
  Subjects: 12
  Sessions per subject: 1
  Events: 0=100, 1=101
  Trial interval: (0, 0.25) s
  File format: EEGLAB .set

Acquisition
-----------
  Sampling rate: 500.0 Hz
  Number of channels: 32
  Channel types: eeg=32
  Channel names: C3, C4, CP1, CP2, CP5, CP6, Cz, F10, F3, F4, F7, F8, F9, FC1, FC2, FC5, FC6, Fp1, Fp2, Fz, O1, O2, Oz, P10, P3, P4, P7, P8, P9, Pz, T7, T8
  Montage: standard_1020
  Hardware: BrainProducts LiveAmp
  Reference: FCz
  Ground: FPz
  Sensor type: EEG
  Line frequency: 50.0 Hz
  Impedance threshold: 25.0 kOhm
  Cap manufacturer: BrainProducts
  Cap model: Acticap
  Electrode type: active

Participants
------------
  Number of subjects: 12
  Health status: healthy
  Age: mean=30.6, std=7.1
  Gender distribution: female=4, male=8
  Species: human

Experimental Protocol
---------------------
  Paradigm: cvep
  Task type: visual attention
  Number of classes: 2
  Class labels: 0, 1
  Trial duration: 2.2 s
  Study design: factorial design (code type × amplitude depth)
  Study domain: BCI performance and user experience
  Feedback type: none
  Stimulus type: visual flashing
  Stimulus modalities: visual
  Primary modality: visual
  Synchronicity: synchronous
  Mode: offline
  Training/test split: False
  Instructions: focus on four targets that were cued sequentially in a random order for 0.5 s, followed by a 2.2 s stimulation phase, before a 0.7 s inter-trial period
  Stimulus presentation: display=Dell P2419HC LCD monitor, resolution=1920×1080 pixels, refresh_rate=60 Hz, brightness=265 cd/m², stimulus_size=150 pixels, background_luminance=124 lux (50% screen luminance), on_state_100=168 lux (100% amplitude depth), on_state_40=142 lux (40% amplitude depth), cue_duration=0.5 s, stimulation_duration=2.2 s, inter_trial_interval=0.7 s

HED Event Annotations
---------------------
  Schema: HED 8.4.0 | Browse: https://www.hedtags.org/hed-schema-browser

  0
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Label/intensity_0

  1
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Label/intensity_1

Paradigm-Specific Parameters
----------------------------
  Detected paradigm: cvep
  Code type: m-sequence (maximum-length sequence)
  Code length: 132
  Number of targets: 4

Data Structure
--------------
  Trials: 60
  Blocks per session: 15
  Trials context: 15 blocks × 4 trials (one per target) × 4 conditions (burst/mseq × 100%/40%)

Preprocessing
-------------
  Data state: raw

Signal Processing
-----------------
  Classifiers: Convolutional Neural Network (CNN)
  Feature extraction: Sliding windows (250ms, 2ms stride), Standard deviation normalization
  Spatial filters: 16 spatial filters via 1D spatial convolution (8×1 kernel)

Cross-Validation
----------------
  Method: sequential train/test split
  Evaluation type: offline classification

Performance (Original Study)
----------------------------
  Accuracy: 85.0%
  Itr: 48.7 bits/min
  Selection Time S: 1.5
  Cnn Training Time 6Blocks S: 40.0
  Calibration Data 6Blocks S: 52.8

BCI Application
---------------
  Applications: reactive BCI
  Environment: laboratory
  Online feedback: False

Tags
----
  Pathology: Healthy
  Modality: EEG
  Type: reactive BCI, visual evoked potentials

Documentation
-------------
  Description: 4-class code-VEP BCI dataset comparing burst c-VEP and m-sequence stimulation at two amplitude depths (100% and 40%) to optimize performance and user experience
  DOI: 10.1016/j.neuroimage.2023.120446
  Associated paper DOI: 10.1016/j.neuroimage.2023.120446
  License: CC-BY-4.0
  Investigators: Kalou Cabrera Castillos, Simon Ladouce, Ludovic Darmet, Frédéric Dehais
  Senior author: Frédéric Dehais
  Contact: kalou.cabrera-castillos@isae-supaero.fr
  Institution: Institut Supérieur de l'Aéronautique et de l'Espace (ISAE-SUPAERO)
  Department: Human Factors and Neuroergonomics
  Address: 10 Av. Edouard Belin, Toulouse, 31400, France
  Country: FR
  Repository: Zenodo
  Data URL: https://zenodo.org/record/8255618
  Publication year: 2023
  Funding: AID (Powerbrain project), France; AXA Research Fund Chair for Neuroergonomics, France; Chair for Neuroadaptive Technology, Artificial and Natural Intelligence Toulouse Institute (ANITI), France
  Ethics approval: Ethics committee of the University of Toulouse (CER approval number 2020-334); Declaration of Helsinki
  Keywords: Code-VEP, Reactive BCI, CNN, Amplitude depth reduction, Visual comfort

External Links
--------------
  Source: https://zenodo.org/record/8255618
  Github Code: https://github.com/neuroergoISAE/burst_codes
  Paper: https://doi.org/10.1016/j.neuroimage.2023.120446

Abstract
--------
The utilization of aperiodic flickering visual stimuli under the form of code-modulated Visual Evoked Potentials (c-VEP) represents a pivotal advancement in the field of reactive Brain–Computer Interface (rBCI). This study introduces an innovative variant of code-VEP, referred to as 'Burst c-VEP', involving the presentation of short bursts of aperiodic visual flashes at a deliberately slow rate, typically ranging from two to four flashes per second. The proposed solutions were tested through an offline 4-classes c-VEP protocol involving 12 participants. The full amplitude burst c-VEP sequences exhibited higher accuracy, ranging from 90.5% (with 17.6 s of calibration data) to 95.6% (with 52.8 s of calibration data), compared to its m-sequence counterpart (71.4% to 85.0%). The mean selection time for both types of codes (1.5 s) compared favorably to reports from previous studies. Lowering the intensity of the stimuli only slightly decreased the accuracy of the burst code sequences to 94.2% while leading to substantial improvements in terms of user experience.

Methodology
-----------
Factorial experimental design with 12 healthy participants. EEG recorded with BrainProducts LiveAmp 32-channel system at 500 Hz. Four conditions tested: burst c-VEP and m-sequence c-VEP, each at 100% and 40% amplitude depth. Participants focused on cued targets (4 classes) in 15 blocks of 4 trials per condition. CNN-based decoding with 250ms sliding windows. Subjective ratings collected for visual comfort, mental tiredness, and intrusiveness. VEP analysis included amplitude, latency, and inter-trial coherence metrics.

References
----------
Kalou Cabrera Castillos. (2023). 4-class code-VEP EEG data [Data set]. Zenodo.(dataset). DOI: https://doi.org/10.5281/zenodo.8255618

Kalou Cabrera Castillos, Simon Ladouce, Ludovic Darmet, Frédéric Dehais. Burst c-VEP Based BCI: Optimizing stimulus design for enhanced classification with minimal calibration data and improved user experience,NeuroImage,Volume 284, 2023,120446,ISSN 1053-8119 DOI: https://doi.org/10.1016/j.neuroimage.2023.120446

Notes

.. versionadded:: 1.1.0
Appelhoff, S., Sanderson, M., Brooks, T., Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Hochenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A. and Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. Journal of Open Source Software 4: (1896). https://doi.org/10.21105/joss.01896

Pernet, C. R., Appelhoff, S., Gorgolewski, K. J., Flandin, G., Phillips, C., Delorme, A., Oostenveld, R. (2019). EEG-BIDS, an extension to the brain imaging data structure for electroencephalography. Scientific Data, 6, 103. https://doi.org/10.1038/s41597-019-0104-8

---
Generated by MOABB 1.5.0 (Mother of All BCI Benchmarks)
https://github.com/NeuroTechX/moabb
