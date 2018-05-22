# CryptoDredge

## Overview

CryptoDredge is a simple in use and highly optimized cryptocurrency mining software. It takes full advantage of modern NVIDIA graphics cards through the use of unique optimization techniques. We have also devoted great attention to stable power consumption. These benefits, along with the very small devfee, make our product one of the best publicly available miners.

## Requirements

### Hardware

- GeForce 9, 10 series NVIDIA graphics card and NVIDIA GeForce 750, 750Ti
- Intel or AMD processor with 64-bit support
- 2GB of RAM (4GB recommended). Some alogithms such as neoscrypt require the virtual memory (swap file) with the same size as all of the GPU's memory.
- Internet connection

### Windows

- Microsoft Windows 7 with Service Pack 1 (64-bit), Windows 8.1 (64-bit), or Windows 10 Version 1511 or later (64-bit)
- The latest NVIDIA driver supporting at least CUDA 9.1
- Visual Studio 2017 redistributable. [Download link](https://www.microsoft.com/en-US/download/details.aspx?id=48145)

## Quickstart

The current version of CryptoDredge is a (portable) console application. Unpack the downloaded archive and edit one of the sample `.bat` files or provide the necessary command line arguments.

### Command line arguments

```
-h, -help
Show help

-V, -version
Display the miner version

-a, -algo
Specify the hash algorithm to use

-o, -pool
A mining pool network address

-u, -user
Mining pool authentication username

-p, -pass
Mining pool authentication password/parameter

-i, -intensity
Mining intensity. In opposite to some other tools (CCMiner), we use a small
range of intensity - 0..6

-b, -benchmark
Start the benchmark

-d, -device
List of device ids for mining
```

## Troubleshooting

### Antivirus software reports
CryptoDredge is not a piece of malicious software. You may try to add an exception in antivirus software you use.

### Rejected Shares.
There are many reasons for rejected shares. The primary reasons are:
- high network latency
- overloaded mining server
- aggresive graphics card overclocking
