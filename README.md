# Gozero ORU Miner

ORU mining downloads for the Gozero pool. This is an independent project and is not an official RIGOR release.

## Downloads

Download binaries from [Releases](https://github.com/AlexZeroZero/Gozero-ORU-Miner/releases).

| Package | Platform | Hardware |
| --- | --- | --- |
| Gozero-ORU-GPU-1.1.1-Setup.exe | Windows 10/11 x64 | NVIDIA SM80+ (Ampere or newer) |
| gozero-oru-linux-x64-v1.tar.gz | Linux x86_64, glibc 2.38+ | CPU |

The Linux package in this release is a CPU miner, not a GPU miner. The Windows package includes a graphical interface.

## Windows

Install version 1.1.1, select pool mode, set `https://rgr.pool.gozero.trade/rpc`, then enter your own public ORU address (`rg1q...`) and a unique worker name. No wallet private key is required. Keep TLS verification enabled.

## Linux

On Ubuntu 24.04, install the runtime dependencies:

```sh
sudo apt-get install libcurl4t64 libjansson4
tar -xzf gozero-oru-linux-x64-v1.tar.gz
chmod +x gozero-oru-miner
./gozero-oru-miner --gozero-pool -a rgrpow01 \
  -o https://rgr.pool.gozero.trade/rpc \
  -u YOUR_RG1Q_ORU_ADDRESS.rig01 -p x -t 2 -s 2
```

Use your own public address and change `-t` for the desired CPU thread count. Accepted shares are not mined blocks. Live pool details and rules: https://pool.gozero.trade/ORU

## Verification and source

Compare downloads with `SHA256SUMS.txt`. Corresponding source is included in the release as `Gozero-ORU-GPU-1.1.1-GUI-Source.zip` and `gozero-oru-source-v1.tar.gz`. See the source packages for license notices, dependencies and build instructions. Mining components derived from RIGOR use GPL-2.0-or-later; original notices are preserved.

This repository hosts release downloads and documentation only. It contains no wallet keys, server credentials or production ledger data.
