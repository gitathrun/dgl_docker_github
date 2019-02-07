# Deep Graph Library (DGL) Docker Image for Development #

Author: Teng Fu

## Base Image ##
This is the docker image for DGL development, its baseImage is:

__FROM tftwdockerhub/gpu-pytorch:latest__

## Additional installed packages ##

For DGL development:

-  [dgl](https://docs.dgl.ai/index.html), version 0.1.3 until Feb 2019.

>>>Deep Graph Library (DGL) is a Python package built for easy implementation of graph neural network model family, on top of existing DL frameworks (e.g. PyTorch, MXNet, Gluon etc.).

>>>DGL reduces the implementation of graph neural networks into declaring a set of functions (or modules in PyTorch terminology). In addition, DGL provides:

>>>- Versatile controls over message passing, ranging from low-level operations such as sending along selected edges and receiving on specific nodes, to high-level control such as graph-wide feature updates.

>>>- Transparent speed optimization with automatic batching of computations and sparse matrix multiplication.

>>>- Seamless integration with existing deep learning frameworks.

>>>- Easy and friendly interfaces for node/edge feature access and graph structure manipulation.
>>>- Good scalability to graphs with tens of millions of vertices.

Demo:

>>>![ALT](https://docs.dgl.ai/_images/sphx_glr_1_first_001.png "DGL Example")

>>>![ALT](https://s3.us-east-2.amazonaws.com/dgl.ai/tutorial/1_first/mailbox.png "Computation Graph")

## Environment Setup for DGL ##
Documentation for [DGL Environment](https://docs.dgl.ai/env_var.html)

## Docker Registry Repo ##

-  tftwdockerhub/dgl_docker_dev:latest

## Usage ##

on dsvm-gpu virtual machines


```
sudo docker pull tftwdockerhub/dgl_docker_dev:latest
```

remember the target port is __8889__
```
sudo nvidia-docker run -it -p 8889:8888 -v \<project-dir-path\>:/app tftwdockerhub/dgl_docker_dev:latest
```

In local browser, remember the target port is __8889__ and the token string on CLI screen
```
http://\<vm-ipaddress-or-dns\>:8889/?token=21c5e12xxxxxx
```