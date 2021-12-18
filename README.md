# Reinforcement Learning with Stable Baselines 3

## Development Environment

|      Feature       |        Specification         |
| :----------------: | :--------------------------: |
|  Operating System  | Windows 11 (Build 22000.376) |
|    WSL Version     |              2               |
| WSL Kernal Version |          5.10.60.1           |
|       WSL OS       |      Ubuntu 20.04.3 LTS      |
|  Anaconda (conda)  |            4.11.0            |

## Setup Steps

1. Create the environment with conda.

        conda create -n rl python==3.9

2. Install `PyTorch`. 
    
    Refer to [PyTorch Website](https://pytorch.org) if you want to install a different verion or are working with different OS.

        conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch

    *Note*: cudatoolkit is only needed if you wish to have GPU support for PyTorch. 

3. (Optional for GPU support on WSL 2) Install GPU driver [NVIDIA CUDA-enabled driver for WSL](https://developer.nvidia.com/cuda/wsl).

    Refer to [Enable NVIDIA CUDA on WSL 2 | Microsoft Docs](https://docs.microsoft.com/en-us/windows/ai/directml/gpu-cuda-in-wsl) for more information.

4. Install some more prerequisites.

        sudo apt install cmake swig python-opengl gcc ffmpeg

5. Install Stable Baselines 3 and OpenAI Gym.

        conda activate rl
        pip install stable-baselines3[extra] box2d box2d-kengz gym[box2d] gym[atari]