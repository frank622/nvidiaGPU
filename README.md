### GenAI-focused NVIDIA GPU Overview

| Release Date | Micro Architecture | Notes | Key Models|
|-------|---------|---------|---------|
| 2006 | Tesla | 90nm |  |
| 2010 | Fermi | 40/28nm |  |
| 2012 | kepler | 28nm,GPU Direct  | k40/k80 |
| 2014 | Maxwell | 28nm | M80 |
| 2016 | Pascal | 16nm,Gen1 Nvlink,HBM2,fp16 | p100,GTX1080ti |
| 2017 | Volta | 12nm,Gen2 Nvlink,Gen1 Tensor Cores| v100 |
| 2018 | Turing |12nm,Gen2 Tensor Cores,Gen1 RT cores,int4/8 | T4,GTX2090 |
| 2020 | Ampere |7nm,Gen3 Nvlink,Gen3 Tensor Cores,Gen2 RT cores,Gen1 MIG,TF16/TF32/BF16,HBM2e| A100,A10,GTX3090 |
| 2022 | Hopper|TSMC 4N，Gen4 Nvlink,Gen4 Tensor Cores,Gen2 MIG,FP8 (E5M2/E4M3),Gen1 Transformer Engine,HBM3/HBM3e | H100,H20 |
| 2022 | Ada Lovelace|TSMC 4N,Gen3 RT cores| L40s,GTX4090 |
| 2024 | Blackwell| TSMC 4NP,Gen5 Nvlink,Gen5 Tensor Cores,Gen2 Transformer Engine,FP4,Gen4 RT cores| B100/GH200/GB200,GTX5090 |
| 2026 | Rubin|TSMC 3nm,HBM4| R? |


### Ampere Architecture GPU Specifications

| Parameter | A100 | A100 PCIe | A800 | A800 PCIe | A10 | RTX 3090 |
|-----------|------|-----------|------|-----------|-----|----------|
| **Form Factor** | SXM | PCIe | SXM | PCIe | PCIe | PCIe |
| **FP16** | 300/600T | 300/600T | 300/600T | 300/600T | 125T/250T | 35.6T |
| **TF32** | 156/312T | 156/312T | 156/312T | 156/312T | 62.5T/125T | 17.8T |
| **FP64** | 19.5T | 19.5T | 19.5T | 19.5T | - | - |
| **Memory Capacity** | 80GB HBM2e | 80GB HBM2e | 80GB HBM2e | 80GB HBM2e | 24GB GDDR6 | 24GB GDDR6X |
| **Memory Bandwidth** | 2 TB/s | 2 TB/s | 2 TB/s | 2 TB/s | 600 GB/s | 936 GB/s |
| **Interconnect Bandwidth** | NVLink 600GB/s | PCIe 64GB/s | NVLink 400GB/s | PCIe 64GB/s | PCIe 64GB/s | PCIe 64GB/s |
| **TDP** | 400W | 300W | 400W | 300W | 150W | 350W |



### Hopper Architecture GPU Specifications

| Parameter | H20 Standard | H20 Large Memory | H200 | H100 | H100 PCIe | H800 | H800 PCIe |
|-----------|--------------|------------------|------|------|-----------|------|-----------|
| **Form Factor** | SXM | SXM | SXM | SXM | PCIe | SXM | PCIe |
| **FP16** | 148T | 148T | 1000/2000T | 1000/2000T | 800/1600T | 1000/2000T | 800/1600T |
| **TF32** | 59.8T | 59.8T | 495/989T | 495/989T | 378/756T | 495/989T | 378/756T |
| **FP64** | - | - | 67T | 67T | 51T | 1000T | 800T |
| **Memory Capacity** | 96GB HBM3 | 141GB HBM3e | 141GB HBM3e | 80GB HBM3 | 80GB HBM3 | 80GB HBM3 | 80GB HBM3 |
| **Memory Bandwidth** | 4 TB/s | 4.8 TB/s | 4.8 TB/s | 3.35 TB/s | 2 TB/s | 3.35 TB/s | 2 TB/s |
| **Interconnect Bandwidth** | NVLink 900GB/s | NVLink 900GB/s | NVLink 900GB/s | NVLink 900GB/s | PCIe 128GB/s | NVLink 400GB/s | PCIe 128GB/s |
| **TDP** | 400W | 400W | 700W | 700W | 350W | 700W | 350W |

### Ada Architecture GPU Specifications

| Parameter | L40S | L40 | L20 | L4 | L2 | RTX 4090 | RTX 4090D |
|-----------|------|-----|-----|----|----|----------|-----------|
| **Form Factor** | PCIe | PCIe | PCIe | PCIe | PCIe | PCIe | PCIe |
| **FP16** | 366/733T | 181/362T | 119.5T | 121/242T | 96.5T | 165/330T | 147/294T |
| **TF32** | 181/366T | 90.5/181T | 59.8T | 60.5/121T | 48.3T | 82.6/165.2T | 73.5/147T |
| **FP64** | - | - | - | - | - | - | - |
| **Memory Capacity** | 48GB GDDR6x | 48GB GDDR6x | 48GB GDDR6x | 24GB GDDR6x | 24GB GDDR6x | 24GB GDDR6x | 24GB GDDR6x |
| **Memory Bandwidth** | 864 GB/s | 864 GB/s | 864 GB/s | 300 GB/s | 300 GB/s | 1 TB/s | 1 TB/s |
| **Interconnect Bandwidth** | PCIe 64GB/s | PCIe 64GB/s | PCIe 64GB/s | PCIe 64GB/s | PCIe 64GB/s | PCIe 64GB/s | PCIe 64GB/s |
| **TDP** | 350W | 300W | 275W | 72W | 72W | 450W | 425W |


### Blackwell Architecture GPU Specifications

| Parameter | GB300 | B300 | GB200 | B200 | B100 | RTX 5090 | 5090D |
|-----------|-------|------|-------|------|------|----------|-------|
| **Form Factor** | Multi-chip | SXM | Multi-chip | SXM | SXM | PCIe 5.0 | PCIe 5.0 |
| **FP16** | 5/10P | 2.25/4.5P | 5/10P| 2.25/4.5P| 1.8/3.5P | 210/420T | 150/297T |
| **TF32** | 2.5/5P| 1.12/2.25P | 2.5/5P| 1.12/2.25P| 0.9/1.8P | 1.25/32P | 1/16P |
| **FP64** | 90T | 40T | 90T | 40T | 30T | - | - |
| **Memory Capacity** | 576GB HBM3e | 288GB HBM3e | 384GB HBM3e | 192GB HBM3e | 192GB HBM3e | 32GB GDDR7 | 32GB GDDR7 |
| **Memory Bandwidth** | 16 TB/s | 8 TB/s | 16 TB/s | 8 TB/s | 8 TB/s | 1.8 TB/s | 1.8 TB/s |
| **Interconnect Bandwidth** | NVLink 3.6 TB/s | NVLink 1.8 TB/s | NVLink 3.6 TB/s | NVLink 1.8 TB/s | NVLink 1.8 TB/s | PCIe 128GB/s | PCIe 128GB/s |
| **TDP** | 1400W | 1400W | 2700W | 1000W | 700W | 575W | 575W |

