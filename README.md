# cdsdashboards-jupyter-docker

Automatic builds of Jupyter Docker images with [ContainDS Dashboards](https://github.com/ideonate/cdsdashboards) support.

These are based on the [Jupyter docker stacks](https://github.com/jupyter/docker-stacks)

voila (Using Voila as the presentation type)

- [jh-voila-oauth-singleuser](https://hub.docker.com/r/ideonate/jh-voila-oauth-singleuser) (Standard Python environment)
- [jh-voila-oauth-scipy](https://hub.docker.com/r/ideonate/jh-voila-oauth-scipy) (Extra scientific Python packages installed)
- [jh-voila-oauth-datascience](https://hub.docker.com/r/ideonate/jh-voila-oauth-datascience) (More than just Python)
- [jh-voila-oauth-r](https://hub.docker.com/r/ideonate/jh-voila-oauth-r) (R language)

all (Using either Voila, Streamlit, Bokeh/Panel, or Plotly Dash as the presentation type)

- [containds-all-basic](https://hub.docker.com/r/ideonate/containds-all-basic) (Standard Python environment)
- [containds-all-scipy](https://hub.docker.com/r/ideonate/containds-all-scipy) (Extra scientific Python packages installed)

r (Using Voila or R Shiny Server)

- [containds-rshiny](https://hub.docker.com/r/ideonate/containds-rshiny) (R environment)

allr (Using a full combination of all the Python and R Shiny presentation types)

- [containds-allr-datascience](https://hub.docker.com/r/ideonate/containds-allr-datascience) (SciPy plus R environment)

There is a tag for each commit SHA in this repo, and also a tag for each release of [ContainDS Dashboards](https://github.com/ideonate/cdsdashboards).

For example, use ideonate/containds-all-basic:0.0.20 as the singleuser image if your JupyterHub is running cdsdashboards version 0.0.20.

