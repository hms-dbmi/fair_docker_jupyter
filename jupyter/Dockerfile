FROM jupyter/datascience-notebook:latest

ADD update_os.sh update_os.sh
RUN sh update_os.sh

ADD update_os2.sh update_os2.sh
RUN sh update_os2.sh

ADD dependencies.r dependencies.r
RUN Rscript dependencies.r

ADD dependencies2.r dependencies2.r
RUN Rscript dependencies2.r

RUN rm dependencies*.r
RUN rm update_os*.sh

USER root

