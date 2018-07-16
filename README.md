# CryptoDredge

## Overview

CryptoDredge is a simple in use and highly optimized cryptocurrency mining software. It takes full advantage of modern <span style="color:#76b900">NVIDIA</span> graphics cards through the use of unique optimization techniques. We have also devoted great attention to stable power consumption. These benefits, along with the very small developer fee, make our product one of the best publicly available miners.

## Features

Developer fee is 1%

## Supported Algorithms

- Allium
- Blake (2s)
- Lyra2REv2
- Lyra2z
- NeoScrypt
- PHI1612
- Phi2
- Skunkhash
- Skein

## QuickStart

The current version of CryptoDredge is a (portable) console application. Unpack the downloaded archive and edit one of the sample `.bat`/`.sh` files or provide the necessary command line arguments.

### Sample Command Line

```
CryptoDredge -a <ALGO> -o stratum+tcp://<POOL> -u <WALLET_ADDRESS> -p <OPTIONS>
```

## Command-Line Arguments

`-v`, `--version` Print version information

`-a`, `--algo` Specify algorithm to use
- `allium`
- `blake2s`
- `lyra2v2`
- `lyra2v2-old` (see the _Lyra2REv2 Issues_ item)
- `lyra2z`
- `neoscrypt`
- `phi`
- `phi2`
- `skein`
- `skunk`

`-d`, `--device` List of comma-separated device IDs to use for mining. IDs are numbered `0,1`...,N - 1

`-h`, `--help` Print help information

`-i`, `--intensity` Mining intensity (0 - 6) (default: `6`)

`-o`, `--url` URL of mining pool

`-p`, `--pass` Password/Options for mining pool

`-u`, `--user` Username for mining pool

`--log` Log output to file

`--no-color` Force color off

`--no-watchdog` Force watchdog off

`--cpu-priority` Set process priority in the range 0 (low) to 5 (high) (default: `3`)

`--api-type` Specify API type to use (default: `ccminer-tcp`)
- `ccminer-tcp` (TCP)
- `ccminer-ws` (WebSocket)
- `off`

`-b`, `--api-bind` IP:port for the miner API, 0 disabled (default: `127.0.0.1:4068`)

`--retries` N number of times to retry if a network call fails, 0 retry indefinitely (default: `0`)

`--retry-pause` N time to pause between retries, in seconds (default: `15`)

`--timeout` N network timeout, in seconds (default: `30`)

## System Requirements

- <span style="color:#76b900">NVIDIA</span> GPUs with Compute Capability 5.0 or above
- Latest GeForce driver
- 2GB of RAM (4GB recommended). Some algorithms such as neoscrypt require the virtual memory (swap file) with the same size as all of the GPU's memory.
- Internet connection

### Windows

- Windows 7/8.1/10 (64-bit versions)
- [Visual C++ Redistributable for Visual Studio 2015](https://www.microsoft.com/en-US/download/details.aspx?id=48145)

### Linux

- Ubuntu 14.04+, Debian 8+ (64-bit versions)
- Package libc-ares2. Installing libc-ares2 package is as easy as running the following command on terminal:
```
apt-get install libc-ares2
```

## Troubleshooting

### Antivirus Software Reports

CryptoDredge is not a piece of malicious software. You may try to add an exception in antivirus software you use.

### Rejected Shares.

There are many reasons for rejected shares. The primary reasons are:
- high network latency
- overloaded mining server
- aggresive graphics card overclocking

### Watchdog

If you are using a third-party watchdog, you can disable the built-in watchdog by using `--no-watchdog` option.

### Lyra2REv2 Issues

In case if you have issues with the current implementation of Lyra2REv2 (lyra2v2), you might want to try lyra2v2-old.
```
CryptoDredge -a lyra2v2-old -o stratum+tcp://<POOL> -u <WALLET_ADDRESS>
```

### Contact

If you have problems, questions, ideas or suggestions, please contact us by posting to cryptodredge@gmail.com

### Web Site

Visit the CryptoDredge web site for the latest news and downloads: [https://cryptodredge.org/](https://cryptodredge.org/)
