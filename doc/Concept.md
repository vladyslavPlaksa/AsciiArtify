# Concept

This document provides a comparative analysis of three tools for deploying Kubernetes clusters in a local environment: minikube, kind, and k3d. Each of these tools has its own characteristics, advantages and disadvantages, which will be discussed below.

## Characteristics

|                           |Minikube                                                                                                    |Kind (Kubernetes IN Docker)                                       |K3D                                                                                                                                   |
|---------------------------|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
|Supported OS               |Linux, macOS, Windows, Docker, VirtualBox, QEMU, Podman, Hyper-V, KVM                                       |Linux, macOS, Windows, Docker                                     |Linux                                                                                                                                 |
|Possibility of automation  |Yes ✅                                                                                                      |Yes ✅                                                             |Yes ✅                                                                                                                                |
|Additional features        |Kubernetes cluster monitoring and management                                                                |Nope 🚫                                                           |  Kubernetes cluster monitoring and management                                                                                        |
|Docker license             |Potential issues with Docker Desktop license for Windows and macOS                                          |Potential issues with Docker Desktop license for Windows and macOS|Potential issues with Docker Desktop license for Windows and macOS                                                                    |
|Advantages                 |Easy to use. Has community support and documentation. The ability to monitor and manage a Kubernetes cluster|Easy to use. Possibility of automation. Can be used with Docker   |Speed deployment and testing of Kubernetes clusters. Possibility of automation. The ability to monitor and manage a Kubernetes cluster|
|Disadvantages              |Limited scaling capabilities. Possible licensing issues with Docker Desktop for Windows and macOS           |Lack of additional functions                                      |Possible licensing issues with Docker Desktop for Windows and macOS                                                                   |

## Conclusions

In the context of the PoC for the AsciiArtify startup, the recommended tool for deploying a local Kubernetes cluster is k3d. It provides rapid deployment and testing of Kubernetes clusters, automation capability, and support for cluster monitoring and management. Also, bearing in mind possible problems with the Docker license for Windows and macOS, it is worth considering an alternative - Podman, which can be used with k3d to work with containers.

### Related info about K3D

![Image](../.data/651332.gif)

#### [K3D installation scripts](https://k3d.io/v5.6.0/#installation)
#### [Guide](https://k3d.io/v5.6.0/usage/configfile/)