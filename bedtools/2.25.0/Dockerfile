#################################################################
# Dockerfile
#
# Version:          2
# Software:         Bedtools
# Software Version: 2.25.0
# Description:      A powerful toolset for genome arithmetic
# Website:          https://github.com/arq5x/bedtools2
# Tags:             Genomics
# Provides:         Bedtools 2.25.0
# Base Image:       biodckr/biodocker
# Build Cmd:        docker build biodckrv/bedtools 2.25.0/.
# Pull Cmd:         docker pull biodckr/bedtools
# Run Cmd:          docker run biodckr/bedtools
#################################################################

# Source Image
FROM biodckr/biodocker

################## BEGIN INSTALLATION ###########################

# install
RUN conda install bedtools=2.25.0

# Change workdir to /data/
WORKDIR /data/

# Define default command
CMD ["bedtools"]

##################### INSTALLATION END ##########################

# File Author / Maintainer
MAINTAINER Saulo Alves Aflitos <sauloal@gmail.com>
# Modified by Felipe da Veiga Leprevost 06-17-2016
