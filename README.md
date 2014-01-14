## Ghost Dockerfile


This repository contains **Dockerfile** of [Ghost](https://www.ghost.org/) for [Docker](https://www.docker.io/)'s [trusted build](https://index.docker.io/u/dockerfile/ghost/) published to the public [Docker Registry](https://index.docker.io/).


### Dependencies

* [dockerfile/nodejs](http://dockerfile.github.io/#/nodejs)


### Installation

1. Install [Docker](https://www.docker.io/).

2. Download [trusted build](https://index.docker.io/u/dockerfile/ghost/) from public [Docker Registry](https://index.docker.io/): `docker pull dockerfile/ghost`

   (alternatively, you can build an image from Dockerfile: `docker build -t="dockerfile/ghost" github.com/dockerfile/ghost`)


### Usage

    docker run -d -p 80:2368 dockerfile/ghost

#### Customize Ghost server by attaching override directory

    docker run -d -p 80:2368 -v <override-dir>:/ghost-override dockerfile/ghost

where `<override-dir>` is an absolute path of a directory that could contain:

  - `config.js`: custom config file
  - `content/data`: persistent/shared data
  - `content/themes`: more themes
  - *or anything else you want to override...*

After few seconds, open `http://<host>` for blog or `http://<host>/ghost` for admin page.
