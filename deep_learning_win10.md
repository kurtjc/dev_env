### Before everything

Different libraries (tensorflow, pytorch, etc.) might rely on different versions of CUDA & CUDNN, check them first and find a common version that work for all.


### CUDA

Assuming CUDA 9.0, CUDNN 7.0

* Install visual studio 2017 with visual c++ 2015
* download CUDA installer from Nvidia website
* install CUDA, do custom install
	* uncheck drivers -- they should have already been installed
	* uncheck "visual studio integration" -- otherwise the installation may fail
* download CUDNN
* unzip CUDNN, and put the dll, h, lib files in the **corresponding directories in the installed CUDA**

---

### Tensorflow

Follow official website should work --> use pip3

---

### Pytorch

Follow official website should work --> use pip3
