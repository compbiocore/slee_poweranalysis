FROM cowmoo/rnaseq_rstudio:latest
RUN apt-get update
RUN apt-get install -y libxt6 liblzma-dev libbz2-dev libz-dev
RUN R -e "BiocManager::install(c('RnaSeqSampleSize'))"
RUN R -e "BiocManager::install(c('rmarkdown', 'fitdistrplus'))"
RUN cd /home/rstudio && git clone https://github.com/compbiocore/slee_poweranalysis.git
RUN chmod 777 -R /home/rstudio/slee_poweranalysis/