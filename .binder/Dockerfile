FROM rocker/binder:3.6.0
LABEL maintainer='Elena Lopez'
USER root
COPY . ${HOME}
RUN chown -R ${NB_USER} ${HOME}
USER ${NB_USER}



RUN wget https://github.com/ElenaBioLung/test1/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2019-09-19/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
