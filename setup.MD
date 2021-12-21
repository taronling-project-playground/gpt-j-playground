## System specifications

### Hardware

- CPU: Ryzen 9 5950X
- GPU: RTX A6000
- Motherboard: MSI Meg X570
- RAM: 128GB

### Software

- Ubuntu 20.04
- CUDA: 11.2 (
    $ sudo apt update
    $ sudo apt install nvidia-cuda-toolkit
)
- CuDNN: 7.6.5 (https://developer.nvidia.com/rdp/cudnn-archive#a-collapse765-101)

## Installation Issues (Off memory)

- Could not load libraries.
    - Make sure files are all added to path properly. May need to reboot the machine for these changes to take effect. See possible fixes below:
    - Anaconda may also be a possible solution, though I did not try this as I prefer managing all my environments.
    - https://stackoverflow.com/questions/64880546/tensorflow-could-not-load-dynamic-library-libcudart-so-10-0-on-ubuntu-18-04
    - https://github.com/tensorflow/tensorflow/issues/20271
    - https://stackoverflow.com/questions/67805919/problem-with-setting-up-tensorflow-gpu-support (Ignore the comment about clean installing ubuntu, that did not appear to be necessary)

- Display driver conflicts
    - Update display drivers. (https://www.cyberciti.biz/faq/ubuntu-linux-install-nvidia-driver-latest-proprietary-driver/)

- sm_86 support for pytorch.
    - Install nightly pytorch. (https://github.com/pytorch/pytorch/issues/52288)