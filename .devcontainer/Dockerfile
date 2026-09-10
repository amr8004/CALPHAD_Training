FROM continuumio/miniconda3

RUN apt-get update \
    && apt-get install -y gcc \
    && conda install -y -c conda-forge "nim>2" \
    && conda install -y -c conda-forge python=3.11 liblapack jupyter numpy pandas plotly scikit-learn \
    && pip install scheil
    && pip install pycalphad

WORKDIR /workspace