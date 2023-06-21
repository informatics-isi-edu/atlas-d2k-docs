---
title: Command lines and libraries
permalink: /docs/command-lines-and-libraries/
---

The ATLAS-D2K repository can be accessed programmatically through command line interfaces and libraries.

## Libraries 
* python client library
* R client library
* [js client library](https://github.com/informatics-isi-edu/ermrestjs)

## Deriva Client tools 
Install deriva-client:
- For folks that have python3 installed run: `pip install deriva-client`  
- For Windows/Mac users who want bundles, download here: https://github.com/informatics-isi-edu/deriva-client-bundle/releases/latest
- General information on deriva-client here: https://github.com/informatics-isi-edu/deriva-client  

## Command lines 

### Download an exported BDBAG through command lines
- Download and install Deriva.py 
- Download the appropriate export configs  
  - [RNASeq Replicates](https://github.com/informatics-isi-edu/gudmap-rbk/blob/master/config/replicate_export_config.json)
  - Note: all our configs can be found [here](https://github.com/informatics-isi-edu/gudmap-rbk/tree/master/config).
- Run the deriva-download-cli commands: 
```
usage: deriva-download-cli [-h] [--version] [--quiet] [--debug]
                           [--credential-file <file>]
                           [--token <auth-token> | --oauth2-token <oauth2-token>]
                           [--catalog <1>]
                           <host> <config file> <output dir> [<key=value key=value>]
```
For example:
```
> mkdir deriva-downloads
> deriva-download-cli www.gudmap.org --catalog 2 ./replicate_export_config.json ./deriva-downloads rid=16-1ZX4
```
