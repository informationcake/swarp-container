# A containerised version of the mosaicking software SWARP

**The SWARP website is here:** https://www.astromatic.net/software/swarp/

**The SWARP Github page is here:** https://github.com/astromatic/swarp

**The SWARP documentation (PDF download):** https://raw.githubusercontent.com/astromatic/swarp/legacy_doc/prevdoc/swarp.pdf

**Use this webpage to obtain the fields required for a certain mosaic:** https://dr12.sdss.org/mosaics/


## How to build and run the container

Clone this repository

Build the image

    docker build . -f ./Dockerfile --tag swarp:latest

Run the container

    docker run --name swarp -d -t -v "$(pwd)"/scripts:/opt/scripts/ swarp:latest

Exec into the container

    docker exec -it swarp /bin/bash

Run the .sh script in scripts

### Options

Verbose is set to FULL, but you can change this inside the script
