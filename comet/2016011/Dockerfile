#################################################################
# Dockerfile
#
# Version:          1
# Software:         Comet
# Software Version: 2016011
# Description:      basic local alignment search tool
# Website:          http://comet-ms.sourceforge.net/
# Tags:             Proteomics
# Provides:         Comet 2016011
# Base Image:       biodckr/biodocker:latest
# Build Cmd:        docker build --rm -t biodckr/comet 2016011/.
# Pull Cmd:         docker pull biodckr/comet
# Run Cmd:          docker run --rm biodckr/comet comet
#################################################################

# Set the base image to biodckr/biodocker
FROM biodckr/biodocker:latest

################## BEGIN INSTALLATION ###########################

USER biodocker

RUN ZIP=comet_binaries_2016011.zip && \
    wget https://github.com/BioDocker/software-archive/releases/download/Comet/$ZIP -O /tmp/$ZIP && \
    unzip /tmp/$ZIP -d /home/biodocker/bin/Comet/ && \
    chmod -R 755 /home/biodocker/bin/Comet/comet_binaries_2016011/* && \
    rm /tmp/$ZIP

RUN mv /home/biodocker/bin/Comet/comet_binaries_2016011/comet.2016011.linux.exe /home/biodocker/bin/Comet/comet

ENV PATH /home/biodocker/bin/Comet:$PATH

WORKDIR /data/

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Felipe da Veiga Leprevost <felipe@leprevost.com.br>
