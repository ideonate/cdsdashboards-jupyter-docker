ARG BASE_REPO=jupyterhub/singleuser
FROM $BASE_REPO

RUN rm -rf /home/jovyan/work

RUN conda install --quiet --yes -c conda-forge voila

RUN pip install jhsingle-native-proxy

COPY voila-entrypoint.sh /opt/conda/bin

