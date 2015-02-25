cxxnet
======

CXXNET (spelled as: C plus plus net) is a fast, concise, distributed deep learning framework.

Contributors: https://github.com/antinucleon/cxxnet/graphs/contributors

[Documentation and Tutorial](doc)

Feature Highlights
=====
* Lightweight: small but sharp knife 
  - cxxnet contains concise implementation of state-of-art deep learning models
  - The project maintains a minimum dependency that makes it portable and easy to build
* Scale beyond single GPU and single machine
  - The library works on multiple GPUs, with nearly linear speedup
  - THe library works distributedly backed by disrtibuted parameter server
* Easy extensibility with no requirement on GPU programming
  - cxxnet is build on [mshadow](#backbone-library)
  - developer can write numpy-style template expressions to extend the library only once
  - mshadow will generate high performance CUDA and CPU code for users
  - It brings concise and readable code, with performance matching hand crafted kernels

### Backbone Library
CXXNET is built on [MShadow: Lightweight CPU/GPU Tensor Template Library](https://github.com/tqchen/mshadow)
* MShadow is an efficient, device invariant and simple tensor library
  - MShadow allows user to write expressions for machine learning while still provides 
  - This means developer do not need to have knowledge on CUDA kernels to extend cxxnet.
* MShadow also provides a parameter interface for Multi-GPU and distributed deep learning
  - Improvements to cxxnet can naturally run on Multiple GPUs and being distributed

Build
=====
* Copy ```make/config.mk``` to root foler of the project
* Modify the config to adjust your enviroment settings
* Type ```make``` to build cxxnet
