# Prerequisites for Software

中文版本：

[软件先决条件](https://www.notion.so/1d133900bc8780b6a358c9838f2a8306?pvs=21)

Back to Table of Contents:

[Getting Started](https://www.notion.so/Getting-Started-1b433900bc8780c4a503e3490ce3e718?pvs=21)

## Hardware Requirements

To ensure codec performance, as well as inference performance, make sure that your onboard computer has the following minimum operating requirements:

| Components | Minimum Requirements | Used for | Reasoning |
| --- | --- | --- | --- |
| CPUs | 4 Cores | Video streaming for remote teleoperation and image compression of dataset creation | These operations use software codecs, and low CPU performance can result in encoding frame rates not keeping up with camera frame rates |
| RAM | 8 GB | Dataset creation cache | Camera images are cached in memory for a period of time before being written to disk |
| GPU | NVIDIA RTX2060 | Inference of VLA models | AhaRobot uses NVIDIA GPUs for inference acceleration |

## Software Requirements

The main part of AhaRobot runs on ROS2 Humble and employs Docker to isolate the main system. Make sure you have the following software components installed on your onboard computer:

| Components | Installation Instructions |
| --- | --- |
| Ubuntu 24.04.1 Desktop | [https://ubuntu.com/download/desktop](https://ubuntu.com/download/desktop) |
| Docker | [https://docs.docker.com/engine/install/ubuntu/](https://docs.docker.com/engine/install/ubuntu/) |
| NVIDIA Container Toolkit | [https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html) |
| Sunshine (recommended) | [https://docs.lizardbyte.dev/projects/sunshine/latest/md_docs_2getting__started.html](https://docs.lizardbyte.dev/projects/sunshine/latest/md_docs_2getting__started.html)
Every time you reboot your system, you need to start the service in the terminal with this command: `systemctl --user restart sunshine && DISPLAY=:0 xhost local: +` |

Continue reading the next section:

[Flashing Firmware](https://www.notion.so/Flashing-Firmware-1d133900bc87807c9070f3c6736d68b7?pvs=21)