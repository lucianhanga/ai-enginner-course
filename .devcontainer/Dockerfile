FROM jupyter/datascience-notebook:latest

USER jovyan
WORKDIR /home/jovyan

# Create virtual environment
RUN python -m venv venv

# Install basic packages in virtual environment
RUN /home/jovyan/venv/bin/pip install --upgrade pip
RUN /home/jovyan/venv/bin/pip install ipykernel

# Install Jupyter kernel for the virtual environment
RUN /home/jovyan/venv/bin/python -m ipykernel install --user --name venv --display-name "AI Engineer (Python)"

# Set environment variables
ENV VIRTUAL_ENV=/home/jovyan/venv
ENV PATH=/home/jovyan/venv/bin:$PATH
