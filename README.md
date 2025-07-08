# AI Engineer Course

This repository contains the workspace setup for the AI Engineer course, configured with Jupyter notebooks and data science tools.

## Quick Start

### Option 1: Using Dev Containers (Recommended)

1. Make sure you have Docker running
2. Install the "Dev Containers" extension in VS Code
3. Open this folder in VS Code
4. When prompted, click "Reopen in Container" or use Command Palette > "Dev Containers: Reopen in Container"
5. The container will build a custom Docker image that automatically sets up:
   - A dedicated virtual environment named `venv` in the project folder
   - All required Python packages installed
   - Jupyter kernel configured for the virtual environment
6. **Important**: When opening notebooks, make sure to select the "AI Engineer (Python)" kernel

### Option 2: Local Setup

If you prefer to work locally:

```bash
# Create a virtual environment
python -m venv venv

# Activate the virtual environment
# On macOS/Linux:
source venv/bin/activate
# On Windows:
# venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Start Jupyter Lab
jupyter lab
```

## What's Included

- **Jupyter Data Science Notebook environment** with Python 3.9+
- **Dedicated Virtual Environment** (`venv`) with isolated package management
- **Pre-installed libraries**:
  - pandas, numpy, matplotlib, seaborn (data analysis & visualization)
  - scikit-learn, tensorflow, pytorch (machine learning)
  - jupyterlab, plotly (interactive notebooks)
- **VS Code extensions** for Python and Jupyter development
- **Custom Jupyter kernel** ("AI Engineer (Python)") linked to the virtual environment
- **Sample notebook** (`getting-started.ipynb`) to test the setup

## Files Structure

```
ai-enginner-course/
├── .devcontainer/
│   ├── devcontainer.json          # Dev container configuration
│   └── Dockerfile                 # Custom Docker image with virtual environment
├── venv/                          # Virtual environment (created automatically)
├── getting-started.ipynb          # Sample Jupyter notebook
├── requirements.txt               # Python dependencies
└── README.md                      # This file
```

## Troubleshooting

### Dev Container Issues

If you encounter issues with the dev container:

1. **Check Docker**: Ensure Docker Desktop is running
2. **Rebuild Container**: Command Palette > "Dev Containers: Rebuild Container"
3. **Clear Cache**: Command Palette > "Dev Containers: Rebuild Without Cache"
4. **Build Issues**: If the Docker build fails, check that `requirements.txt` is present in the project root

### Local Setup Issues

If you have issues with local setup:

1. **Python Version**: Ensure you're using Python 3.8+
2. **Virtual Environment**: Always use a virtual environment to avoid conflicts
3. **Dependencies**: If specific packages fail to install, try installing them individually

## Getting Help

- Check the VS Code Dev Containers documentation
- Verify Docker is running and accessible
- For course-specific questions, refer to your course materials

Happy coding! 🚀
