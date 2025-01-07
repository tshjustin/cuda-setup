# cuda-setup
Setting up CUDA on GPU devices 

1. Check if GPU exist on device (can view via Task Manager)

2. Run the following in terminal   
```
nvidia-smi 
```

# Example O/P 
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 496.76       Driver Version: 496.76       CUDA Version: 11.5     |
|-------------------------------+----------------------+----------------------+
| GPU  Name            TCC/WDDM | Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  NVIDIA GeForce ... WDDM  | 00000000:01:00.0  On |                  N/A |
| N/A   56C    P0    28W /  N/A |    999MiB /  6144MiB |      5%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+

+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|


3. Download CUDA toolkit & nvcc (Ensure comptability with GPU present): https://developer.nvidia.com/cudnn


4. run the given script 

Alternatively, if using `venv`, one can do the following with the venv activated (example)

```
conda search -c nvidia cuda-toolkit # Check for NVIDIA CUDAs 

conda install cudatoolkit=xx.x -c nvidia # Install CUDA from NVIDIA Channel 

conda install -c nvidia cuda-nvcc=xx.x # Install nvidia CUDA compiler (nvcc) (Ensure compatibility)

conda install pytorch torchvision torchaudio -c pytorch # Install PyTorch with CUDA xx.x Support
```