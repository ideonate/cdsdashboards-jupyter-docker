ARG BASE_REPO=ideonate/jh-voila-oauth-singleuser
FROM $BASE_REPO

USER $NB_UID

RUN pip install streamlit

RUN pip install dash plotlydash-tornado-cmd>=0.0.4

RUN pip install bokeh panel bokeh-root-cmd>=0.0.5

# Leave user as jovyan to avoid accidental container runs as root
