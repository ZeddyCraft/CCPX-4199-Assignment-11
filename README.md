# CCPX-4199-Assignment-11
# Random Dot Motion (RDM) Task & Performance Visualization

This repository contains a PsychoPy file that does a Random Dot Motion (RDM) perceptual decision-making task, along with automated post-task data visualization.

## Overview of the Experimental Task
The Random Dot Motion paradigm measures visual motion perception and decision-making under varying levels of sensory uncertainty:

1. **Setup & Instructions:** Collects participants' info (`participant_nr`, `age`, and `number of trials`) via a dialog box, initializes a PsychoPy window, and presents the task instructions.
2. **Stimulus Presentation:** On each trial, a variable fixation cross will appear before flipping to a circular aperture containing 150 moving dots (`DotStim`).
3. **Experimental Conditions:** Trials vary across **5 motion coherence levels** (`5%`, `10%`, `20%`, `40%`, and `80%`) and **2 motion directions** (`0°` Right and `180°` Left), randomized via PsychoPy's `TrialHandler`.
4. **Response & Data Logging:** Participants indicate the perceived motion direction using the `left` or `right` arrow keys. Trial-by-trial accuracy, reaction time (RT), coherence, direction, and fixation duration are saved to an Excel file in the following format:(`<participant_nr>_random_dot_motion.xlsx`).

## Data Visualization
After finishing the experiment, `pandas` and `matplotlib` are used to generate a boxplot visualization of the participant's reaction time by the motion coherence:
- **X-Axis (Coherence Level):** The 5 motion coherence levels (`0.05`, `0.1`, `0.2`, `0.4`, `0.8`) representing increasing signal strength.
- **Y-Axis (Reaction Time):** The distribution of response times (in seconds) at each coherence level, displaying the median, interquartile range (IQR), and outliers.
