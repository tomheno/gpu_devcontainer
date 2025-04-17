FROM nvcr.io/nvidia/pytorch:25.03-py3

# Install Ollama
RUN curl -fsSL https://ollama.com/install.sh | TERM=xterm sh

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install python3 python3-venv python3-pip

RUN python3 -m venv /workspace/venv
ENV PATH="/workspace/venv/bin:$PATH"

# Set working directory
WORKDIR /workspace

# Install IPython kernel and its dependencies
RUN pip install ipykernel && \
    python -m ipykernel install --user --name python3 --display-name "Python 3.12.8"

# Note: requirements.txt will be installed after container creation
CMD [ -f "requirements.txt" ] && pip install -r requirements.txt || echo "No requirements.txt found"