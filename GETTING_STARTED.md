# Getting Started with Pose-Independent 3D Anthropometry

Welcome! This guide will help you get started with the **Pose-Independent 3D Anthropometry** repository.

## 🚀 Quick Start

### Option 1: Interactive Jupyter Notebook (Recommended)
1. **Open the notebook**: `getting_started.ipynb`
2. **Run all cells** to explore the repository interactively
3. **Follow the step-by-step guide** with visualizations and examples

### Option 2: Command Line Setup
```bash
# Install dependencies
pip install torch numpy pandas matplotlib seaborn pyyaml tqdm scipy scikit-learn

# Explore the repository structure
ls -la

# Check the configuration
cat configs/config_real.yaml

# View the model architecture
python -c "from models import SimpleMLP; print(SimpleMLP())"
```

## 📋 What This Repository Does

**Goal**: Estimate 11 body measurements from 70 body landmarks of a posed subject.

**Key Innovation**: Works with any pose, not just standard A-pose!

### Measurements Estimated:
1. Ankle Circumference
2. Arm Length (Shoulder to Elbow)
3. Arm Length (Shoulder to Wrist)
4. Arm Length (Spine to Wrist)
5. Chest Circumference
6. Crotch Height
7. Head Circumference
8. Hip Circ Max Height
9. Hip Circumference, Maximum
10. Neck Base Circumference
11. Stature (Height)

## 🏗️ Repository Structure

```
pose-independent-anthropometry/
├── getting_started.ipynb          # 👈 START HERE!
├── configs/config_real.yaml       # Configuration file
├── models.py                      # SimpleMLP model definition
├── train.py                       # Training script
├── evaluate.py                    # Evaluation script
├── dataset.py                     # Dataset classes
├── utils.py                       # Utility functions
├── data/                          # Data directory
├── results/                       # Pre-trained models
└── scripts/                       # Data processing scripts
```

## 🎯 Typical Workflow

1. **Explore** → Open `getting_started.ipynb`
2. **Setup** → Install dependencies and download required models
3. **Data** → Prepare datasets using scripts in `scripts/`
4. **Train** → Run `python train.py` to train your own model
5. **Evaluate** → Use `python evaluate.py` to test performance
6. **Analyze** → Compare results with paper benchmarks

## 📚 Supported Datasets

- **CAESAR**: Commercial dataset with ~4,400 subjects
- **DYNA**: Free dynamic sequences (10 subjects)
- **4DHumanOutfit**: Free clothed sequences (6 subjects)

## 🔧 Key Commands

```bash
# Training
python train.py

# Evaluation (various scenarios)
python evaluate.py CAESAR_STAND -R results/2024_07_11_09_42_48
python evaluate.py CAESAR_POSED -R results/2024_07_11_09_42_48
python evaluate.py DYNA -R results/2024_07_11_09_42_48

# Monitoring training
visdom -p 8080  # Then open http://localhost:8080
```

## 🎓 Learning Path

### Beginner
- Start with `getting_started.ipynb`
- Understand the model architecture
- Run simulated examples

### Intermediate
- Set up real datasets
- Train your own model
- Evaluate on different poses

### Advanced
- Modify model architecture
- Add new feature transformations
- Extend to new datasets

## 📖 Additional Resources

- **Paper**: [Pose-independent 3D Anthropometry from Sparse Data](https://inria.hal.science/hal-04683475/file/eccv_2024_pose_independent_anthropometry_camera_ready.pdf)
- **SMPL Models**: https://smpl.is.tue.mpg.de/
- **DYNA Dataset**: http://dyna.is.tue.mpg.de/
- **4DHumanOutfit**: https://kinovis.inria.fr/4dhumanoutfit/

## 🆘 Need Help?

1. **Check the notebook**: Most questions are answered in `getting_started.ipynb`
2. **Read the paper**: Detailed methodology and results
3. **Examine the code**: Well-documented Python files
4. **Check configurations**: `configs/config_real.yaml` has all parameters

## 🎉 Ready to Start?

Open `getting_started.ipynb` and begin your journey into pose-independent anthropometry!

---

*This repository implements the ECCV 2024 paper "Pose-independent 3D Anthropometry from Sparse Data"*