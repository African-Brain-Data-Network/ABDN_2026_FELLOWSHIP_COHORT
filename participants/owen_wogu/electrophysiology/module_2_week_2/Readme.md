**Week 2 Assignment Draft: One-Pager of Experimental Design**

Title: 
Assessment of the Delta/Alpha Power Ratio of the Single-Lead Frontal Channel Pair 
(Fp1–Fp2) as a Cost-Effective Method for Seizure Diagnosis in Resource-Poor Populations

Research Question
In freely available datasets of scalp EEG from pediatric patients, is the ratio of
delta-to-alpha power of the single-lead frontal channel pair (Fp1–Fp2) significantly 
higher among epileptic children than in age-equivalent controls.

Background and Rationale:
Epilepsy among children is very common in Sub-Saharan Africa; however, the 19 channel, 
high-density clinical EEG machines are not affordable, too technical, and incompatible
with unreliable grid electricity. The current literature indicates that the use of 
complex deep learning and graph attention models leads to the problem of black box
interpretation and computational burden that makes them impractical in off-grid environments
Testing the validity of the interpretability and efficacy of a single lead frontal spectral
slowing biomarker (delta/alpha ratio) ensures a low-cost basis for future diagnostic devices.

Study Design:
A retrospective case-control computational study performing secondary analysis of
de-identified human EEGs. Publicly available human EEG.

**Participants or Model**

Model System: 
Non-invasive electroencephalography (EEG) recordings acquired from human pediatric 
scalp samples (aged 5–12 years)

Inclusion/Exclusion Criteria:
Case subjects are pediatric patients who have clinical diagnosis of focal epilepsy; control 
subjects are age-matched healthy subjects20. Records with significant and uncorrectable movement 
artifact or lack of channel metadata information are excluded

Sample Size Estimation:
Using G*Power 3.1 software for power calculation in independent two-tailed t-test sample size 
calculation, N = 52 subjects (Ncases = 26, Ncontrols = 26) must be obtained in order to obtain 
80% statistical power (beta = 0.20) for significance level of alpha = 0.05, medium to large 
effect size (Cohen's d = 0.70) from pediatric interictal EEG research.

**Recording Method**

Data Collection: 
Scalp EEG recordings based on Brain Imaging Data Structure (BIDS) standard will be collected from 
publicly available sources (OpenNeuro/PhysioNet)26more_horiz.

Channel and Signal Processing: 
Raw signals will be trimmed to focus only on the Fp1-Fp2 frontal leads45. Processing in MNE-
Python involves 0.5-45 Hz bandpass filter and adaptive 50 Hz notch filter for elimination of 
local powerline interference.

Power Spectral Features Extraction: 
Interictal delta-to-alpha power ratio will be calculated using Welch's periodogram method to 
obtain Power Spectral Density (PSD) from Delta (1-4 Hz) and Alpha (8-12 Hz) frequency bands.

Controls and Blinding
Negative Control: EEG recordings of age-matched healthy pediatric controls determine the baseline 
spectral power in background conditions.

Positive Reference Standard: Detailed 19 channel clinical EEG annotations in the dataset metadata 
are used as the gold standard diagnosis

Anonymizing/blinding:
The single blind computational protocol entails using codes that are anonymized for signal pre-
processing and features extraction. Therefore, the analyst does not know the disease status until 
statistical analysis

Ethical Considerations: 
This project involves the reanalysis of completely anonymized publically available data that 
falls within IRB exemption category. The use of the data complies with the open repositories 
licensing policy and African health data ethics to prevent unattributed use of such data.

Data Management Plan: 
Data management plan conforms to the BIDS guidelines for EEG. Following the FAIR guideline 
principles (findable, accessible, interoperable, reusable), preprocessing code and Jupyter 
notebook and calculated PSD ratios will be openly deposited on Github.
