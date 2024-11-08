FROM rocker/r-ver:4.4.1

RUN mkdir /home/example

COPY install.R /home/example/install.R
COPY script.R /home/example/script.R

RUN R -e "options(repos = \
  list(CRAN = 'https://cloud.r-project.org')); \
  source('/home/example/install.R')"

CMD R -e "source('/home/example/script.R')"