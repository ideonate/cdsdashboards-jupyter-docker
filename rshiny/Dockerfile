ARG BASE_REPO=ideonate/jh-voila-oauth-r
FROM $BASE_REPO

USER root

# From repo2docker buildpack
RUN curl --silent --location --fail https://download3.rstudio.org/ubuntu-14.04/x86_64/shiny-server-1.5.12.933-amd64.deb > /tmp/shiny.deb && \
                echo '9aeef6613e7f58f21c97a4600921340e /tmp/shiny.deb' | md5sum -c - && \
                dpkg -i /tmp/shiny.deb && \
                rm /tmp/shiny.deb

# Switch back to jovyan to avoid accidental container runs as root; also pip doesn't need root
USER $NB_UID

RUN pip install 'rshiny-server-cmd>=0.0.2'

