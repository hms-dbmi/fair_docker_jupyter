FROM aguidetti/r-datascience-notebook:latest

ADD dependencies.r dependencies.r
RUN Rscript dependencies.r
ADD dependencies2.r dependencies2.r
RUN Rscript dependencies2.r

ADD nhanes_rcupcake_quickstart.ipynb nhanes_rcupcake_quickstart.ipynb

RUN rm dependencies*.r
