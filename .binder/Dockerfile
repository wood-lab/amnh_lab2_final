FROM rocker/binder:3.6.0
LABEL maintainer='Maureen Anne Williams'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}
RUN wget https://github.com/wood-lab/amnh_lab2_final/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-08-28/')); devtools::install_deps()"
