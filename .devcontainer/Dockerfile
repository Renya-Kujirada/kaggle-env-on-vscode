FROM kaggle/python-gpu-build
# FROM gcr.io/kaggle-gpu-images/python
RUN pip install torch==1.12.1+cu116 torchvision==0.13.1+cu116 torchaudio==0.12.1 --extra-index-url https://download.pytorch.org/whl/cu116 \
    && pip install autopep8 \
    && pip install black \
    && pip install samplerate

# RUN pip install -U pip \
#     && pip install --no-cache-dir japanize_matplotlib \
#     && pip install --no-cache-dir torchviz \
#     && pip install --no-cache-dir torchinfo \
#     && pip install --no-cache-dir mlflow \
#     && pip install --no-cache-dir autopep8 \
#     && pip install --no-cache-dir ipywidgets \
#     && pip install --no-cache-dir transformers[ja] \
#     && pip install --no-cache-dir sentencepiece \
#     && pip install --no-cache-dir tokenizer \
#     && pip install --no-cache-dir iterative-stratification \
#     && jupyter nbextension enable --py widgetsnbextension

# RUN apt-get update && apt-get install -y \
#     screen

# RUN conda install graphviz \
#     && conda clean -i -t -y

# work in container rootless.
# RUN useradd -m -d /home/dev-user -s /bin/bash dev-user
# USER dev-user
USER jupyter

# save gpu session between local and container.
# CMD screen watch -n 1 nvidia-smi
