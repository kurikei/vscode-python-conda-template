FROM continuumio/miniconda3
COPY environment.yaml .
RUN pip install --upgrade pip && \
    conda config --remove channels defaults  && \
    conda config --add channels conda-forge && \
    conda env create -n app -f environment.yaml && \
    conda init && \
    echo "conda activate app" >> ~/.bashrc