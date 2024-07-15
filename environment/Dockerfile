# hash:sha256:36d0eeffb5b3535ce45df6ce113d950378577d4bb260f540653afad8f23fec46
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/jupyterlab:3.0.9-miniconda4.9.2-python3.8-ubuntu20.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN pip3 install -U --no-cache-dir \
    scikit-learn==1.3.2

COPY postInstall /
RUN /postInstall
