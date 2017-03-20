# Companion

A portable, scalable eukaryotic genome annotation pipeline implemented in Nextflow.

This repository contains a fork of [companion](https://github.com/sanger-pathogens/companion), 
a pipeline for automatic eukaryotic parasite annotation by the Sanger Institute. 

See [companion.sanger.ac.uk](http://companion.sanger.ac.uk) for documentation and more information. 

The purpose of this fork is to study numerical stability and replicability of bioinformatics 
pipelines across different executions platforms.
 

### [Requirements](#requirements)

The pipeline is built on [Nextflow](http://nextflow.io) as a workflow engine, so it needs to be installed first:
```
export NXF_VER=0.22.0
curl -fsSL get.nextflow.io | bash
```

With Nextflow installed, the easiest way to use the pipeline is to use the prepared Docker container (https://hub.docker.com/r/satta/companion/) which contains all external dependencies.

```
docker pull sangerpathogens/companion@sha256:0d79b408bc2349c57854582769c2083619a246c0f857d76f928238e6e2640287
```

### [Running the pipeline](#running)

The pipeline has been tested in different Unix-like operating systems with and without [Docker](https://www.docker.com/) containers.


#### Docker based execution  

The pipeline can be launched in any system that has the Docker engine installed with this command: 

```
$ nextflow run cbcrg/companion -revision nbt-docker
```

#### Amazon Linux execution 

The pipeline was executed in Amazon Linux (version 2016.03) by using the following command:

```
$ nextflow run cbrg/companion -revision nbt-awslinux
```

In the Linux image were installed the Companion dependencies listed in [here](Dockerfile). The Amazon AMI 
is publically available in the EU (Dublin) AWS region with the ID `ami-1c364e6f`. 

 
#### Mac OSX execution 

The pipeline was executed in a Mac OSX by using the following command:

```
$ nextflow run cbcrg/companion -revision nbt-macosx
```

In the computer were installed the Companion dependencies listed in [here](Dockerfile).

