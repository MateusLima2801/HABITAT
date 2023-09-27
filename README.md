# How to setup HABITAT

Firstly, I couldn't set it up on Windows. I'm using a Linux machine and followed the tutorials on Habitat-Lab and Habitat-Sim.

Certify yourself of running your scripts from the conda environment created.

If you create a new conda environment while VS Code is running, use the refresh icon on the top right of the Python: Select Interpreter window; otherwise you may not find the environment there as descripted in https://code.visualstudio.com/docs/python/environments

# Bugs

## CUDA device

CUDA is a parallel computing platform and programming model developed by NVIDIA for general computing on their GPUs. Running the example scripts of habitat-lab, it outputs:

```
Platform::WindowlessEglApplication::tryCreateContext(): unable to find CUDA device 0 among 2 EGL devices in total
WindowlessContext: Unable to create windowless context
```

As descripted in https://saturncloud.io/blog/can-i-run-cuda-on-intels-integrated-graphics-processor/#:~:text=However%2C%20CUDA%20can%20only%20run,software%20components%20to%20run%20CUDA:

"CUDA can only run on NVIDIA GPUs. This is because CUDA is tightly integrated with NVIDIA’s hardware, software, and tools. Intel’s integrated graphics processors, on the other hand, are designed for basic graphics processing and do not have the necessary hardware and software components to run CUDA."

My machine especifically run with an Intel GPU: Intel UHD Graphics 620, as seen through the command ` $ hwinfo --gfxcard --short` :

```
graphics card:
                       Intel UHD Graphics 620

Primary display adapter: #19
```
