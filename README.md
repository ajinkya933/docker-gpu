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
