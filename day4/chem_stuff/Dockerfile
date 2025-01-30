# Use Miniconda as the base image
FROM continuumio/miniconda3

# Set the working directory inside the container
WORKDIR /app

# Install git to clone the repository
RUN apt-get update && apt-get install -y git

# Clone the GitHub repository containing the app.py (or pythochem_download.py)
RUN git clone https://github.com/superbash-maker/CSS_2025.git

# Create the Conda environment and install dependencies
RUN conda create -n webd python=3.12 -c bioconda -y && \
    conda activate webd && \
    conda install pip spyder -y && \
    pip install requests pubchempy pandas

# Copy the pythochem_download.py file from the cloned repo to the working directory
WORKDIR /app/CSS_2025
COPY pythochem_download.py /app/

# Set the default command to run the Python script
CMD ["python", "/app/pythochem_download.py"]
