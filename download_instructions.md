# 📦 ECG Analysis System - Download Instructions

## Files in This Project:

1. **app.py** (708 lines) - Main Streamlit application
2. **ecg_simulator.py** (128 lines) - ECG signal generator
3. **hrv_analyzer.py** (176 lines) - Heart rate variability analyzer
4. **arrhythmia_detector.py** (194 lines) - ML-based arrhythmia detector
5. **emotion_classifier.py** (118 lines) - Emotion classification
6. **edge_ai_metrics.py** (101 lines) - Edge AI performance metrics
7. **README.md** - Complete documentation
8. **.streamlit/config.toml** - Streamlit configuration

## Option 1: Manual Setup (Copy Files)

### Step 1: Create Project Directory
```bash
mkdir ecg-analysis-system
cd ecg-analysis-system
```

### Step 2: Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### Step 3: Install Dependencies
```bash
pip install streamlit numpy pandas scikit-learn scipy plotly matplotlib seaborn neurokit2
```

### Step 4: Create .streamlit Directory
```bash
mkdir .streamlit
```

### Step 5: Copy Each File
- Copy the contents of each file from the Replit editor
- Save them with the exact filenames listed above

### Step 6: Run the Application
```bash
streamlit run app.py --server.port 5000
```

---

## Option 2: Quick Setup Script

Save this as `setup.sh` and run it:

```bash
#!/bin/bash

# Create project directory
mkdir -p ecg-analysis-system/.streamlit
cd ecg-analysis-system

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install streamlit numpy pandas scikit-learn scipy plotly matplotlib seaborn neurokit2

# Create config file
cat > .streamlit/config.toml << 'EOF'
[server]
headless = true
address = "0.0.0.0"
port = 5000
EOF

echo "Setup complete! Now copy the Python files and run: streamlit run app.py"
```

---

## Option 3: Using Git (If Available)

If your Replit has git enabled:

```bash
# Initialize git (if not already done)
git init
git add .
git commit -m "Initial commit"

# Push to your GitHub repo
git remote add origin YOUR_GITHUB_URL
git push -u origin main

# Then clone from GitHub anywhere
git clone YOUR_GITHUB_URL
```

---

## Dependencies (requirements.txt)

Create a `requirements.txt` file:

```
streamlit
numpy
pandas
scikit-learn
scipy
plotly
matplotlib
seaborn
neurokit2
```

Then install with:
```bash
pip install -r requirements.txt
```

---

## File Structure

```
ecg-analysis-system/
├── .streamlit/
│   └── config.toml
├── app.py
├── ecg_simulator.py
├── hrv_analyzer.py
├── arrhythmia_detector.py
├── emotion_classifier.py
├── edge_ai_metrics.py
├── README.md
└── requirements.txt
```

---

## Running Locally

```bash
cd ecg-analysis-system
streamlit run app.py --server.port 5000
```

Open browser: `http://localhost:5000`

---

## Troubleshooting

**Issue: NeuroKit2 installation fails**
```bash
# Try installing dependencies separately
pip install numpy scipy pandas
pip install neurokit2
```

**Issue: Port already in use**
```bash
streamlit run app.py --server.port 8501
```

**Issue: Module not found**
```bash
# Make sure all files are in the same directory
# Check that you're in the correct directory
pwd
ls -la
```
