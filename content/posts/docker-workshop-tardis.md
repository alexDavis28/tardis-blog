+++
title = 'Docker Workshop'
date = 2025-02-07T15:15:02Z
summary = 'I ran a Docker Workshop for the Tardis Project at my uni'
draft = false
toc =  true
readTime =  true
autonumber =  false
math =  true
tags =  ["post", "docker", "tardis"]
showTags =  true
hideBackToTop =  false
+++
# Running a Docker workshop
During my time at university I’ve been volunteering with the [Tardis Project](https://tardisproject.uk/), a student led group that provides computing services and support for students looking to learn and practice sysadmin skills in a production-like environment.

We'd been talking about running more workshops on various aspects of system administration and devops - and since I'd previously worked with a lot of Docker containers whilst setting up self hosted services (a personal favourite being [Mealie](https://mealie.io/)) I offered to run one on using docker

## Creating the repository
I worked with [Emily](https://emilymiller.xyz/) on creating a very simple flask app,  example Dockerfil and docker-compose file for the workshop.

We hosted the repo on the Tardis Project gitlab, and it can be found [here](https://git.tardisproject.uk/emily747/docker-workshop-2025).

## Writing the wiki page
I also wrote a Powerpoint presentation for the workshop, walking people through each aspect of the Docker architecture, the contents of which are also available [on the Tardis wiki page](https://wiki.tardisproject.uk/howto:specific:learndocker).
We aimed for people to begin by creating a Docker image and running it with `docker run`, before introducting organising the running of containers with compose.

## Problems
- The Tardis Sandbox VM which we had people connect to for the workshop (to save installing Docker locally) actually used Podamn and just aliased docker. This was largely fine but was a bit unexpected.
- A mysterious Ubuntu bug where Podman would create a network with an invalid CNI version as described [here](https://bugs.launchpad.net/ubuntu/+source/libpod/+bug/2024394). We fixed this by just having all the containers use the default Podman network.
    - Although this did cause a problem for the one person at the workshop who was actually using locally installed Docker

## Running the workshop
The Workshop itself went well, with a good attendance and I was able to introduce several people to Docker. As well as being a good experience in public speaking and an opportunity to share my knowledge, it was nice to be able to contribute a guide to the Tardis wiki.