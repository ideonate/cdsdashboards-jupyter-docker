ARG BASE_REPO=jupyterhub/singleuser
FROM $BASE_REPO

# git is now used to source files for cdsdashboards
RUN conda install --quiet --yes -c conda-forge git voila

RUN rm -rf /home/jovyan/work

RUN pip install 'jhsingle-native-proxy>=0.7.6' 'voila-materialstream>=0.4.0'


USER $NB_UID
COPY jupyter_notebook_config_extra.py /etc/jupyter/
RUN cat /etc/jupyter/jupyter_notebook_config_extra.py >> /etc/jupyter/jupyter_notebook_config.py
RUN rm /etc/jupyter/jupyter_notebook_config_extra.py

COPY voila.json /etc/jupyter

# Install ContainDS JupyterLab extension
RUN pip install jupyter-containds

# Fix permissions on /etc/jupyter as root
USER root
RUN fix-permissions /etc/jupyter/

# Switch back to jovyan to avoid accidental container runs as root
USER $NB_UID
