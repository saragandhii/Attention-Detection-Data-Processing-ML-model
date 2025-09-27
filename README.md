# Attention-Detection-Data-Processing-ML-model

# Attention Detection Using EEG

A brain-computer interface (BCI) project that uses EEG-based attention classification to detect inattention and explore neural entrainment systems designed to optimize attentional engagement.

**Affiliation:** Neurotech@Davis, University of California, Davis  

---

## 📖 Introduction
Attention is a limited cognitive resource, and sustaining focus is increasingly difficult in distraction-rich environments.  
This project leverages EEG data to classify when participants are focused or unfocused while completing cognitive tasks.  

Our long-term goal is to design a **closed-loop system** that uses auditory or visual stimuli to gently guide individuals back into optimal focus states.  

**Potential Applications:**  
- Education (improving classroom focus)  
- Mental health (support for ADHD, attention disorders)  
- Productivity (sustaining focus in work environments)  

---

##Methods

### Experimental Paradigm
- Participants completed a **Stroop task** (color-word matching).  
- Three conditions were tested:  
  1. Standard Stroop task  
  2. Stroop with visual distractions  
  3. Stroop with auditory distractions  
- Each condition lasted **15 minutes**, with **5-minute breaks** in between.  

### Data Collection
- EEG recorded using **OpenBCI Cyton Board**.  
- 3 neurotypical college participants.  
- Electrodes placed at: Fp1, Fp2, F7, F3, F4, F8, C3, C4 (International 10-20 system).  
- Focused on frontal lobe activity (executive function).  

### Pre-Processing
- **Bandpass filter:** 1–40 Hz FIR (via MNE).  
- **Segmentation:**  
  - Baseline = before task  
  - Attention = during task  
- **Feature Extraction:** mean, standard deviation, max, min (across channels & time).  
- **Normalization:** StandardScaler (zero mean, unit variance).  

### Classification
- Support Vector Machine (SVM) with linear kernel, C = 1.  
- Training/test split = 80/20.  
- Achieved **75% accuracy** in classifying attention vs. baseline.  

---

## Results
- Successful detection of attentional state with **75% accuracy**.  
- Demonstrated feasibility of EEG-based focus tracking during real tasks.  
- Next steps:  
  - Real-time detection of attention.  
  - Develop auditory stimuli to guide users back into focus.  
  - Long-term: automated, closed-loop attention-enhancing system.  

---
