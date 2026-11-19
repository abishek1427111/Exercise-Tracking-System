# Exercise Tracking System — Computer Vision Workout Tracker

A desktop fitness tracker using webcam pose estimation to count squats and bicep curls, record activity, estimate calories, and generate workout summaries.

## Features
- Webcam pose estimation and squat/curl repetition counts
- Tkinter interface for name, age and optional email input
- CSV exercise logs and PDF workout summaries
- Rep-count plots using Matplotlib
- Optional SMTP email delivery (requires user configuration)

## Technology
Python, OpenCV, MediaPipe, NumPy, Pandas, Matplotlib, Tkinter, FPDF, SMTP.

## Project structure
```text
Machine-Learning/
  Machine-learning-Code/
    app.py
    requirements.txt
  PPT.pptx
  Report.docx
```
The presentation and report are preserved as provided; review their historical author information before sharing.

## Installation and usage
Requires Python with Tkinter support and an accessible webcam. From the repository root:
```bash
cd Machine-Learning/Machine-learning-Code
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
python app.py
```
On some Linux systems Tkinter must be installed via the OS package manager. The original requirements file includes `tk`, which may not be installable from PyPI on every system. If installation fails, install `opencv-python mediapipe numpy pandas matplotlib fpdf` and ensure Tkinter is installed separately.

The application uses the default webcam (`cv2.VideoCapture(0)`). During the workout, press **Q** to quit or **R** to reset counters (per the source code). It writes `exercise_log.csv` and `exercise_summary.pdf` in the working directory.

## Email configuration
The original source contains placeholder `SENDER_EMAIL` and `SENDER_PASSWORD` values. Email sending will not work until valid credentials are configured. **Never commit actual credentials.** Consider replacing these placeholders with environment variables before enabling email or deploying. Do not share personal SMTP credentials.

## Limitations
Calories are estimates based on hardcoded assumptions. Tracking accuracy depends on webcam placement, lighting and pose detection; no accuracy benchmark was verified in the supplied archive.

## Screenshots
No verified screenshots were supplied. Add screenshots under `docs/screenshots/` after running the desktop app.

## Contributions and attribution
Jointly developed project, republished as an independent copy by **Abishek V**. The original README is retained verbatim as [`ORIGINAL_README.md`](ORIGINAL_README.md) for historical attribution. No original Git history was included in the ZIP.

## License
No standalone license was included. Confirm rights and licensing before public redistribution.
