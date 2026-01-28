ARG VARIANT=3.12-bullseye
FROM mcr.microsoft.com/vscode/devcontainers/python:${VARIANT}

ENV PYTHONUNBUFFERED 1

# Upgrade pip
RUN pip install --upgrade pip

# # Download repository with cbc solver and install it.
RUN rm -f /etc/apt/sources.list.d/yarn.list \
    && apt-get update
RUN apt install -y libglpk-dev libgmp3-dev
RUN apt-get install glpk-utils
RUN apt-get install -y -qq coinor-cbc

