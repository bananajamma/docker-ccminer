# docker-ccminer

A docker container for [ccminer](https://github.com/tpruvot/ccminer.git) including [CUDA](https://hub.docker.com/r/nvidia/cuda/).

## Requirements

 * [docker](https://docs.docker.com/install/)
 * [CUDA](https://developer.nvidia.com/cuda-downloads) on the host
 * [nvidia-docker](https://github.com/NVIDIA/nvidia-docker)

## Usage

### First

Pull the latest build:

```
docker pull bananajamma/ccminer
```

### Running

Example:

```
nvidia-docker run -it --rm --name=ccminer -v /etc/localtime:/etc/localtime:ro bananajamma/ccminer --algo=cryptonight --url=stratum+tcp://gulf.moneroocean.stream:10032 --userpass="4JLN35ooAiU15BX6Rzi6DTWUKsdLALvf6Stx1uLLrYP28scYTAtyjhM3ULkrpCQMQ1BGvn2hSaYGtSzwtPcZhFSwdoFypnBsb6wKfhTGix:x"
```

### Building

If you've clone this repo and made changes:

```
docker build . --tag bananajamma/ccminer
```

## License

MIT

