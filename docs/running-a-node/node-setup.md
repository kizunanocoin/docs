# Node Setup

While you can run a KIZUNANO COIN node by downloading a binary or building from source, it is recommended to use a Docker container. When using the [official Docker images](https://hub.docker.com/r/kizunanocoin/node/tags/), your node will be much easier to upgrade and maintain.

--8<-- "docker-limitations.md"

!!! note "Setup Assumptions"
    The guides found on this site make some basic assumptions that should be understood before continuing:

    - You have a basic understanding of Docker.
    - You are using [KIZUNANO COIN's official Docker images](https://hub.docker.com/r/kizunanocoin/kizunanocoin/tags/) to manage your node. If you decide to use a different method, you will need to be able to fill in the gaps when following along.

---

## Hardware recommendations

--8<-- "hardware-recommendations.md"

---

## Network Ports

The kizunano_node will use two configurable ports throughout its lifecycle. The default values suggested by the [network details](configuration.md#network-details) are below:

--8<-- "network-details-simple.md"

!!! note ""
	By default kizunano_node will attempt to use UPnP. [Troubleshooting information can be found here](troubleshooting.md#troubleshooting-upnp)

---

## Installing Docker
Docker must be installed on the host machine and instructions can be found here: https://docs.docker.com/install/. We recommend installing the latest stable version available.

---

## Pulling the Docker Image 
[![Docker Pulls](https://img.shields.io/docker/pulls/nanocurrency/nano.svg)](https://hub.docker.com/r/kizunanocoin/node/)

The Docker image can be downloaded via `docker pull`. We can either grab the `latest` or a specific version/tag. Not specifying a tag defaults to `latest`. An example of each is found below.

Pulls the latest release of KIZUNANO COIN Node:
```bash
docker pull kizunanocoin/node
```

Pulls a specific version of KIZUNANO COIN node:
```bash
docker pull kizunanocoin/node:V20.0
```

!!! tip
	If you are running in an enterprise environment, it is recommended that you explicitly specify the latest stable version to ensure deterministic containers. A list of tags can be found at the official [KIZUNANO COIN Currency Docker Hub](https://hub.docker.com/r/kizunanocoin/kizunanocoin/tags/).

--8<-- "multiple-node-setups-warning.md"

---

## Starting the Node
With Docker there are basic commands for managing containers. To properly bring the node up, learn these commands beginning with [starting the container](docker-management.md#starting).

!!! info "Advanced Builds"
	For additional options around building the node to run on various platforms, head over to the [Integration Guides Build Options](../integration-guides/build-options.md).

---

## Additional setup
The above instructions cover getting a node up and running with the default configuration settings. Additional setup areas to explore include:

- Learning more about [managing the node in a Docker container](docker-management.md)
- Updating [node configuration options](configuration.md) to enable various features
- Setting up the node to [vote as a representative](voting-as-a-representative.md)
- Finding out how to best [manage your ledger file](ledger-management.md)
