FROM jupyter/datascience-notebook:latest

USER jovyan
WORKDIR /home/jovyan

# Copy requirements file from the project root
COPY requirements.txt /tmp/requirements.txt

# Create virtual environment
RUN python -m venv venv

# Install basic packages in virtual environment
RUN /home/jovyan/venv/bin/pip install --upgrade pip

# Install Jupyter kernel for the virtual environment
RUN /home/jovyan/venv/bin/python -m ipykernel install --user --name venv --display-name "AI Engineer (Python)"

# Install packages from requirements.txt
RUN /home/jovyan/venv/bin/pip install -r /tmp/requirements.txt

# Set environment variables
ENV VIRTUAL_ENV=/home/jovyan/venv
ENV PATH=/home/jovyan/venv/bin:$PATH
