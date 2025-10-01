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
| 2024 | Blackwell| TSMC 4NP,Gen5 Nvlink,Gen5 Tensor Cores,Gen2 Transformer Engine,FP6/FP4,Gen4 RT cores| B100/GH200/GB200,GTX5090 |
| 2026 | Rubin|TSMC 3nm,HBM4| R? |


### Ampere Architecture GPU Specifications

| Parameter | A100 | A100 PCIe | A800 | A800 PCIe | A10 | RTX 3090 |
|-----------|------|-----------|------|-----------|-----|----------|
| **Form Factor** | SXM | PCIe | SXM | PCIe | PCIe | PCIe |
| **FP16** | 312/624T | 312/624T | 312/624T | 312/624T | 125T/250T | -|
| **TF32** | 156/312T | 156/312T | 156/312T | 156/312T | 62.5T/125T | -|
| **FP64** | 9.7T |9.7T| 9.7T | 9.7T | - | - |
| **Memory Capacity** | 40HBM2/80GB HBM2e | 40HBM2/80GB HBM2e  | 80GB HBM2e | 40HBM2/80GB HBM2e| 24GB GDDR6 | 24GB GDDR6X |
| **Memory Bandwidth** | 1,555GB/s/2,039GB/s | 1,555GB/s/1,935GB/s | 1,555GB/s/2,039GB/s| 1,555GB/s/1,935GB/s | 600 GB/s | 936 GB/s |
| **Interconnect Bandwidth** | NVLink 600GB/s | PCIe 64GB/s | NVLink 400GB/s | PCIe 64GB/s | PCIe 64GB/s | PCIe 64GB/s |
| **TDP** | 400W | 300W | 400W | 250W/300W | 150W | 350W |


### Hopper Architecture GPU Specifications

| Parameter | GH200 | H200 | H100 | H100 PCIe | H800 | H800 PCIe | H20 Std | H20 Large Memory |
|-----------|-------|------|------|-----------|------|-----------|---------|------------------|
| **Form Factor** | 1*（H200+Grace）| SXM | SXM | PCIe | SXM | PCIe | SXM | SXM |
| **FP8** | 1,979/3,958T | 1,979/3,958T | 1,979/3,958T | 1670/3,341T | 1979/3958T | 1513/3026T | 296T | 296T |
| **FP16** | 990/1,979T | 990/1,979T  | 990/1,979T | 835/1671T | 989/1979T | 756/1513T | 148T | 148T |
| **TF32** | 494/989T | 495/989T | 495/989T | 417/835T | 495/989T | 378/756T | 74T | 74T |
| **FP64** | 34T | 34T | 34T | 30T | 1T | 0.8T | 1T | 1T |
| **Memory Capacity** | 96/144G HBM3 | 141GB HBM3e | 80GB HBM3 | 94GB HBM2e | 80GB HBM3 | 80GB HBM3 | 96GB HBM3 | 141GB HBM3e |
| **Memory Bandwidth** | 4/4.9TB/s | 4.8 TB/s | 3.35 TB/s | 3.9 TB/s | 3.35 TB/s | 2 TB/s | 4 TB/s | 4.8 TB/s |
| **Interconnect Bandwidth** | NVLink 900GB/s | NVLink 900GB/s | NVLink 900GB/s | PCIe 128GB/s | NVLink 400GB/s | PCIe 128GB/s | NVLink 900GB/s | NVLink 900GB/s |
| **TDP** | - | 700W | 700W | 350W | 700W | 350W | 400W | 400W |

- HGX H200 = 8*Hopper GPU soluton package
- GH200 = Grace CPU+H200 GPU
- GH200 NVL2 fully connects two GH200 Superchips with NVLink
- GH200 NVL32 = 32 * GH200  
- GH200 SuperPod = 256 * GH200


### Ada Architecture GPU Specifications

| Parameter | L40S | L40 | L20 | L4 | RTX 4090 |
|-----------|------|-----|-----|----|----------|
| **Form Factor** | PCIe | PCIe | PCIe | PCIe | PCIe |
| **FP16** | 366/733T | 181/362T | 119.5T | 121/242T | - |
| **TF32** | 181/366T | 90.5/181T | 59.8T | 60.5/121T | - |
| **Memory Capacity** | 48GB GDDR6x | 48GB GDDR6x | 48GB GDDR6x | 24GB GDDR6x | 24GB GDDR6x |
| **Memory Bandwidth** | 864 GB/s | 864 GB/s | 864 GB/s | 300 GB/s | 1 TB/s |
| **Interconnect Bandwidth** | PCIe 64GB/s | PCIe 64GB/s | PCIe 64GB/s | PCIe 64GB/s | PCIe 64GB/s |
| **TDP** | 350W | 300W | 275W | 72W | 450W |


### Blackwell Architecture GPU Specifications

| Parameter | GB300 | GB200| B300 | B200 | RTX 5090 |
|-----------|-------|------|-------|------|------|
| **Form Factor** | 2\*Blackwell Ultra GPUs+1\*Grace CPUs | 2\*Blackwell GPUs+1\*Grace CPUs| 2 Die | 2 Die | PCIe 5.0 |
| **FP4** | 15/20P | 10/20P|  13.5/14.25p | 9/18P|   | 
| **FP8** |  5/10P |  5/10P|  4.5/9P | 4.5/9P|   |
| **FP16/BF16** | 2.5/5P | 2.5/5P| 2.2/4.5P |2.2/4.5P|  | 
| **TF32** | 1.25/2.5P | 1.25/2.5P|  1.1/2.2P | 1.1/2.2P|  | 
| **FP64/TF64** | 1.38T | 40T|  1.2T | 37T|   | 
| **Memory Capacity** | 279GB HBM3e/GB300 NVL72:20TB | 186GB HBM3e/GB200 NVL72:13.5TB | 279GB HBM3e | 180/192GB HBM3e | 32GB GDDR7 | 
| **Memory Bandwidth** | 8 TB/s |8 TB/s | 7.7 TB/s | 8 TB/s | 1.8 TB/s |
| **Interconnect Bandwidth** |NVLink 3.6 TB/s  | NVLink 3.6 TB/s | NVLink 3.6 TB/s | NVLink 1.8 TB/s| PCIe 128GB/s | 
| **TDP** | - | 2700W  | 1100W | 1000W | 575W |  

- HGX B200=8x NVIDIA Blackwell GPUs (AWS p6-b200?)
- HGX B300=8x NVIDIA Blackwell Ultra GPUs
- B200 Superchip,2 Die,2*Blackwell GPU
- GB200 Superchip, 2\*Blackwell GPU+1\*Grace CPU
- GB200 Computer Node is comprised of 2 GB200 Superchips, where each Superchip has 1 Grace CPU and 2 Blackwell GPUs
- GB200 NVL72=32*GB200=18*Compute Node（4\*Blackwell GPUs+2\*Grace CPU）->72\*Blackwell GPUs+36\*Grace CPUs
- GB200 NVL72,This form factor requires approximately 120kW per rack (AWS p6e-gb200?)
- GB200 NVL36\*2, 66kW per rack for a total of 132kW for NVL36 racks * 2(AWS p6e-gb200?)
- GB200 SuperPod=288*GB200
- GB300 NVL72=18*Compute Node（4\*Blackwell Ultra GPUs+2\*Grace CPU）->72\*Blackwell Ultra GPUs+36\*Grace CPUs 
- blackwell-architecture: https://resources.nvidia.com/en-us-blackwell-architecture

> For any questions, please contact me via email: **frank622@gmail.com**
