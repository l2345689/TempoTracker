# TempoTracker
TempoTracker is a proof-of-concept project that uses a smartphone’s built-in accelerometer to detect reps and tempo during workouts.  Most fitness apps only log sets and weights, but ignore the rhythm of training — a critical part of strength progression. TempoTracker explores how raw motion data can capture that missing layer of performance.

## Instructions 🏋️‍♂️

This script analyzes accelerometer data from workouts (squats, pushups, bicep curls) and automatically counts repetitions, splits them into eccentric and concentric phases, and plots the signal.

⸻

 ## 🔧 Requirements

Make sure you have Python 3.8+ installed.
Install dependencies with:
    pip install pandas matplotlib scipy

## 📂 Setup

	1.	Clone this repository:
        
        git clone https://github.com/yourusername/rep-phase-counter.git
cd rep-phase-counter

    2. Place your accelerometer CSV file in the same folder.
Your CSV must have at least these columns:
	•	seconds_elapsed → time values
	•	z → z-axis accelerometer data
Example: 
data.csv contains

seconds_elapsed,z
0.00,9.81
0.02,9.75
0.04,9.60

    3. Open rep_phase_counter.py and edit the user config section at the top:
        # --- USER CONFIG ---
CSV_FILE = "INSERT_YOUR_CSV_HERE.csv"   # replace with your file
EXERCISE = "squat"  # options: "squat", "pushup", "bicep_curl" ## Currently we only offer 3 types of exersizes. 

## ▶Running the Script

Run the script with:  python rep_phase_counter.py

A chart will also appear showing:
	•	Smoothed z-axis signal
	•	Peaks and valleys
	•	Highlighted eccentric (red) and concentric (blue) phases

![Demo](assets/demo.png)


    