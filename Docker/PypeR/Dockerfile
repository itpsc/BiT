FROM bioconductor/release_core2
ADD requirements.txt /tmp
ADD install.R /tmp
RUN Rscript /tmp/install.R && \
pip install -r /tmp/requirements.txt
CMD ["/bin/bash"]
