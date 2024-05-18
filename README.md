# docker-gpu

Steps to connect docker runtime to nvidia backend, so that we can use `nvidia-smi` inside docker container

- Step1: Install nvidia-container-toolkit
```
sudo apt-get install -y nvidia-container-toolkit
```
and see output of `nvcc --version`
```
nvcc --version

nvcc: NVIDIA (R) Cuda compiler driver
Copyright (c) 2005-2021 NVIDIA Corporation
Built on Thu_Nov_18_09:45:30_PST_2021
Cuda compilation tools, release 11.5, V11.5.119
Build cuda_11.5.r11.5/compiler.30672275_0
```
nvidia-smi
```
+---------------------------------------------------------------------------------------+
| NVIDIA-SMI 535.171.04             Driver Version: 535.171.04   CUDA Version: 12.2     |
|-----------------------------------------+----------------------+----------------------+
| GPU  Name                 Persistence-M | Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp   Perf          Pwr:Usage/Cap |         Memory-Usage | GPU-Util  Compute M. |
|                                         |                      |               MIG M. |
|=========================================+======================+======================|
|   0  NVIDIA GeForce GTX 1080 Ti     Off | 00000000:06:00.0  On |                  N/A |
|  0%   45C    P8              18W / 280W |    248MiB / 11264MiB |      3%      Default |
|                                         |                      |                  N/A |
+-----------------------------------------+----------------------+----------------------+
                                                                                         
+---------------------------------------------------------------------------------------+
| Processes:                                                                            |
|  GPU   GI   CI        PID   Type   Process name                            GPU Memory |
|        ID   ID                                                             Usage      |
|=======================================================================================|
|    0   N/A  N/A      1922      G   /usr/lib/xorg/Xorg                           74MiB |
|    0   N/A  N/A      2084      G   /usr/bin/gnome-shell                        134MiB |
|    0   N/A  N/A      2703      G   ...,262144 --variations-seed-version=1       36MiB |
+---------------------------------------------------------------------------------------+
```

## cuda version = 11.5 
note that nvidia-smi command also shows cuda vesion but thats not correct, refer `nvcc --version` for getting correct cuda version
