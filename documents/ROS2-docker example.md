## ROS2 on NVIDIA Jetson with Docker
This guide provides instructions for setting up ROS2 on NVIDIA Jetson devices using pre-built 
Docker containers from the Jetson Zoo. These containers are optimized for Jetson
platforms and simplify the installation process.

Version: ROS Melodic, ROS Noetic, ROS2 Eloquent, ROS2 Foxy, ROS2 Galactic, ROS2 Humble
Supports: JetPack >= 4.2 (Jetson Nano / TX1 / TX2 / Xavier NX / AGX Xavier / AGX Orin)

### 1. Docker Installation 

```python
sudo apt-get update
sudo apt-get install docker.io
sudo systemctl start docker
sudo systemctl enable docker
sudo apt-get install nvidia-docker2
sudo systemctl restart docker
```
### 2: Pull the ROS2 Docker Image
Pull the ROS2 container from the Jetson Zoo. For example, to use ROS2 Foxy:

```python
docker pull dustynv/ros:foxy-pytorch-l4t-r35.1.0
```

### 3: Run the ROS2 Container
Start the container with GPU access:
 
```python
docker run --runtime nvidia -it dustynv/ros:foxy-pytorch-l4t-r35.1.0
```
### 4: Verify ROS2 Installation
Inside the container, verify the ROS2 installation:

```python
source /opt/ros/foxy/setup.bash
ros2 --version
```

### 5: Test GPU Access
Ensure the container has access to the GPU:

```python
nvidia-smi
```


