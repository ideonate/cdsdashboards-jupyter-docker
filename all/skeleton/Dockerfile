ARG BASE_REPO={{TEMPLATE_BASE_REPO}}
FROM $BASE_REPO

USER root

RUN pip install streamlit

RUN pip install dash plotlydash-tornado-cmd

COPY streamlit-entrypoint.sh /opt/conda/bin

COPY plotlydash-entrypoint.sh /opt/conda/bin


# Switch back to jovyan to avoid accidental container runs as root
USER $NB_UID
