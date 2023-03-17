# Description

This repo is associated with the following paper:

> *Trait anxiety is associated with hidden state inference during aversive reversal learning* (2023). O Zika, K Wiech, A Reinecke, M Browning, NW Schuck - Nature Communications, https://doi.org/10.1101/2022.04.01.483303

The repository contains raw data used from the three experiments described in the paper. 

There are two files:
1. The `zika2023_metadata.csv` file contains all meta-level data. That is, one line for each participant-session combination (participants in Study 3 completed three sessions which are shown in three separate lines)
2. The `zika2023_full_behavioural_raw_data.csv` file contains single-trial level data. Some of the information from the meta file is already included in this file. 

Here, I will define the key columns in both files. 

### Meta file 

`zika2023_metadata.csv`

**Columns**

`ids`  participant ID  
`ta` trait anxiety score  
`sb` starting contingency within a session (participants either started with high or low probability of shock)  
`specID` participant ID composed of combination of ID and session, i.e. each line has unique `specID`  
`sh_int` shock intensity calibrated for each session  
`study` which study was the participant part of  
`contingency` the high and low shock probability levels used (60/40, 75/25 and 90/10)  
`order_exact` order of sessions (only in participants who completed 3 sessions)  

### Trial-level file 

`zika2023_full_behavioural_raw_data.csv`

Each Session consisted of three cues presented in random order. For the 'Reversal' cue, it could either be in high or low state (which I refer to as acq/ext sometimes).

**Columns**

`Session` continuous block of trials without a pause (This does not correspond to 60/40, 75/25, 90/10)  
`Reversal_ID` this variable increases every time the hidden contigency of the reversal cue changes  
`Learning_Phase` refers to high (1) or low (2) state   
`Trial` trial within session  
`Trial_Type` 1=stable-high cue, 2=stable-low cue, 3=reversal cue (see also `trial_type_str` for categorical version)  
`Subjective_Probability` submitted rating on a given trial  
`Outcome_Type` 0 = n-shock, 1 = shock (see also `outcome_str` for categorical version)  
`id`  participant ID  
`specID` participant ID composed of combination of ID and session  
`contingency` the high and low shock probability levels used (60/40, 75/25 and 90/10)  
`updates` change in probability rating since last occurrence of a given cue  
`mflr` model-free learning rate on a given trial  
`half`/`half_str` first or second half of the task  
`study_str` which study was the participant part of  

### Author

Ondrej Zika  
@OndrejZika  
[www.ondrejzika.cz](www.ondrejzika.cz)  