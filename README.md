## Pre-Launch Survey Analysis: Voice-to-Text Clinical Notes for EMRs

A Power BI dashboard analysing a pre-launch survey of doctors on how they document in an Electronic Medical Record (EMR) system, and whether they would use a phone app that turns dictation into text they can paste into the EMR.

## Project Overview

Documentation in the EMR takes up a large part of a doctor's day, and notes can be lost when the system crashes. Before building a speech-to-text (STT) tool, I surveyed practising doctors to find out:
<ul>
<li>How much time they spend typing notes, and where documentation slows them down most</li>
<li>How often the EMR crashes or loses notes, and how they cope</li>
<li>How comfortable they are with phone apps and voice dictation</li>
<li>Whether they would use a dictation app, and what would stop them</li>
<li>Whether they accept patient conversations being recorded (with consent)</li>
<li>Which feature would make the tool most useful</li>
</ul>

The goal was to validate demand and identify the requirements and risks before development.

## Data
<ul>	
<li>Source:	Survey form responses, exported to Excel (Voice-to-Text_Clinical_Notes_for_EMRs__Responses_.xlsx)
<li>Respondents:	15 doctors</li>
<li>Roles	House: Officer (5), Registrar (4), Medical Officer (3), Senior Resident (2), Consultant (1)</li>
<li>Questions:	15 (EMR usage, documentation habits, EMR reliability, phone and dictation experience, willingness to use the tool, barriers, preferred setting, recording consent, feature request)</li>
</ul>

The workbook has three sheets:
<ul>
<li>the raw form export (Form Responses 1)</li>
<li>an intermediate sheet (Form_Responses_2)</li> 
<li>the cleaned table (Form_Responses) that feeds the dashboard.</li>
</ul>

## Data Preparation
<ul>
<li>Cleaned and standardised response labels (for example, consistent capitalisation in the "how did you cope" answers)</li>
<li>Reshaped the multi-select "What would stop you from using it?" question to one row per selection, so each barrier can be counted separately (four rows per respondent, padded with "None Selected")</li>
<li>Assigned a Respondent ID to each respondent</li>
<li>Built the data model in Power BI with a single Form_Responses table and DAX measures for the summary cards (willingness to use, prior dictation use, lost notes)</li>
</ul>

## Dashboard

The report has one page, Pre-Launch, with:
<ul>
<li>KPI cards: total respondents, share willing to use the tool, share who have used dictation before, share who have lost notes</li>
<li>A role slicer to filter every visual by seniority</li>
<li>Willingness to use the tool</li>
<li>Number of times respondents have lost notes in the current EMR</li>
<li>Barriers to using the tool</li>
<li>Comfort with patient conversations being recorded (with consent)</li>
<li>Features that would make the tool more useful</li>
<li>Typing time on a typical day</li>
</ul>

## Key Findings
<ul>
<li>Strong demand: 13 of 15 respondents (87%) would "definitely" (10) or "probably" (3) use the app.</li>
<li>Documentation is a real burden: 13 of 15 spend 30 minutes or more a day typing notes, and 5 spend over an hour. Emergencies (7) and ward rounds (6) are the biggest slowdowns.</li>
<li>The EMR loses notes: 13 of 15 (87%) have lost notes at least once, 10 of them "a few times". Network problems and power loss were the causes given, and the most common response was to start the note again.</li>
<li>Paper-first workarounds are common: 9 of 15 write notes on paper first, at least sometimes.</li>
<li>Dictation is new to most: only 4 of 15 have used voice dictation, with mixed accuracy ratings for medical terms and accents.</li>
<li>Accuracy is the main barrier and the top feature request: "Poor accuracy" was the most-selected barrier (10 selections), ahead of extra steps, network or data cost, and slowness (5 each) and privacy (4). Transcription accuracy or clarity was the most requested feature (6 respondents).</li>
<li>Consent to recording is divided: 3 said yes, 7 said "depends", and 5 said no, so consent and confidentiality need careful design.</li>
<li>Mobile-ready users: 12 of 15 are comfortable or very comfortable with phone apps.</li>
</ul>

## Recommendations
<ul>
<li>Prioritise transcription accuracy for medical terminology and local accents, and test it with real clinicians before launch.</li>
<li>Make the app work offline or with low data use, since network and data cost are barriers and network failures already affect EMR use.</li>
<li>Keep the workflow short: dictate, review, then paste into the EMR, with as few extra steps as possible.</li>
<li>Build privacy and consent into the design (clear consent prompts, no unnecessary storage of audio).</li>
<li>Start with ward rounds and clinics, where respondents most want to use it.</li>
</ul>

## Limitations
<ul>
<li>Small sample (n = 15) from a limited set of doctors, so results are directional rather than statistically representative.</li>
<li>Self-reported answers; no usage or accuracy testing of an actual tool.</li>
<li>Barriers were multi-select, so barrier counts are selections, not respondents.</li>
</ul>

## Tools

Power BI (data model, DAX measures, visuals), Excel (data cleaning and reshaping).

## Files
<ul>
<li>File	Description</li>
<li>pre_STT.pbix	Power BI report</li>
<li>Voice-to-Text_Clinical_Notes_for_EMRs__Responses_.xlsx	Survey data (raw and cleaned sheets)</li>
</ul>
