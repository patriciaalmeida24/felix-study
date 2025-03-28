# SOP: EEG recording procedure
## 1.0	EEG endpoints 

App. 20 min recording of EEG should be performed in patients enrolled in FELIX study at two time points: baseline and week 6 (day 42). 
Explorative outcomes include:
1.	Spectral changes in eyes-closed resting state from baseline to week 6. Several aspects, such as frontal asymmetry, slowing of brain rhythms could be demonstrated on depressed patients. Is there more gamma brain activity at resting state and does it correlate to treatment response? 
2.	Changes in 40 Hz SSVEP response from baseline to week 6 and these changes between the 2 treatment groups. Psychiatric disorders have been shown reduced steady state responses and hypothesize to reflect deficits in sensory processing. Neurofeedback has been applied and proven to be helpful in these situations. We could hypothesize that continuous 40 Hz stimulation could result in higher SSVEP response over time. 
3.	Changes in vigilance and association with treatment response: patients with depression show less and later declines into lower EEG vigilance stages during resting states. 

## 2.0 Experimental Paradigm
-	Setting up the EEG is estimated to take 10 minutes. 
-	1 minute of eyes-open resting state EEG recording is done first. 
-	10 minutes of continuous eyes-closed EEG recording is needed for estimating the resting state spectral changes. In case 10 minutes is not possible, try to make at least 5 minutes of quality continuous resting state recording. 
-	3 minutes of 40 Hz strobe is needed for evaluation of SSVEPs response for both patient groups.  
-	Any medication taken before the recording should be recorded (see appendix A)

## 3.0	Recording the EEG
### 3.1 The procedure:
1.	Explain the procedure to the patient and the importance of sitting still and relaxing
2.	Make sure to unplug all devices from the walls and have a quiet, dimmed environment. 
3.	Fill in the EEG recording protocol in the eCRF (see Appendix A)
4.	Prepare the equipment (EVYLIGHT with a strobe setting, MENTALAB cap with electrodes, gel for wet recordings, computer with a license for EEG recorder system, papertowels for the patient to clean up)
5.	Place the electrodes according to the 10-20-system. The electrodes for FELIX measurements are the following: Fp1, Fp2, F1, F2, P1, P2, O1, O2. (Ref = Cz). MENTALAB software requires defining the electrodes every time you turn it on, see below:

[Ch0/GND	| Ref (Cz)],
[Ch1	    | Fp1],
[Ch2	    | Fp2],
[Ch3/Pz	| F1],
[Ch4FpZ	| F2],
[Ch5/O1	| P1],
[Ch6/O2	| P2],
[Ch7/T3	| O1],
[Ch8/T4	| O2]

![image](https://github.com/user-attachments/assets/dda9f7ae-98bc-4423-8a20-0048d2eb9b1a)

6.	Check that the electrode impedance is less than 20 kOhm. When checking impedance the sampling rate changes back into 250Hz. After the impedance check has been completed, change the sampling rate back to 500 Hz in the settings. 
7.	Prepare the EVY LIGHT with a 40 Hz strobe setting for the measurement of SSVEP response 
8.	Apply filters: Apply a bandpass filter from 1-60 Hz and a notch filter at 50 Hz. (!! the applied filter will not affect the saved data. Data are always saved in raw format) 
9.	Start recording
a.	Choose “bdf” format and keep recording time at 3600 s (60 minutes)
10.	First, record 1 minute of eyes open resting state and put sw-1 event trigger on the recording. 
11.	Note any disturbance using the event marking system (sw-66 for any noice) 
12.	Record 10 continuous minutes of good quality eyes closed resting state EEG and mark sw-2 for second event. 
13.	Shortly explain the procedure to the patient again, warn about strobe and let them know that they can stop the experiement at any time if they feel any discomfort 
14.	Record 1 minute of strobe with patients covering their eyes in order to exclude SSVEP due to the noise from the device and mark it sw-3
15.	Record 1 minute of strobe and resting state eyes open interchangebly for 3 times and mark it sw-4. 

### 3.2	Saving and sending the EEG data
The procedure:
1.	Save the recordings in bdf format on the OptoCeutics computer used for EEG recording temporarily. 
2.	Upload the data to a secure external drive and store it for further analysis. 
3.	Keep a local copy of the EEG with patient identification for the GCP- monitor and clinical use.




