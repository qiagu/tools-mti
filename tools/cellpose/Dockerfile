FROM python:3.8-slim

ENV CELLPOSE_VERSION=2.0.5 NUMBA_CACHE_DIR=/tmp CELLPOSE_LOCAL_MODELS_PATH=/.cellpose/models
RUN apt-get update && \
    apt-get install -y --no-install-recommends git unzip wget &&\
    apt-get clean && \
    mkdir -p ${CELLPOSE_LOCAL_MODELS_PATH}

RUN pip install -U pip && \
    pip install --no-cache-dir cellpose==$CELLPOSE_VERSION 'scikit-learn>1.0, \
    <1.1' 'opencv-python-headless>=4.5.1.48' 'scikit-image>0.17, <0.20' \
    'git+https://github.com/goeckslab/model-unpickler.git'

ADD https://www.cellpose.org/models/cytotorch_0 ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/cytotorch_1 ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/cytotorch_2 ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/cytotorch_3 ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/cyto2torch_0 ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/cyto2torch_1 ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/cyto2torch_2 ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/cyto2torch_3 ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/nucleitorch_0 ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/nucleitorch_1 ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/nucleitorch_2 ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/nucleitorch_3 ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/CP ${CELLPOSE_LOCAL_MODELS_PATH}

ADD https://www.cellpose.org/models/size_cytotorch_0.npy ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/size_cyto2torch_0.npy ${CELLPOSE_LOCAL_MODELS_PATH}
ADD https://www.cellpose.org/models/size_nucleitorch_0.npy ${CELLPOSE_LOCAL_MODELS_PATH}
