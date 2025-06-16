FROM jupyter/base-notebook:python-3.10

# Switch to root user
USER root

# Install additional software
RUN apt upgrade -y && \
    apt update -y && \
    apt install -y curl


# Switch to notebook user
USER jovyan

# Install additional Python packages
COPY ./requirements.txt /home/jovyan/requirements.txt
RUN pip install -r /home/jovyan/requirements.txt
