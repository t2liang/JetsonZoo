
## Docker set-up
#### 1. Figure out what Development environment you need and then visit [Jetson Zoo](https://elinux.org/Jetson_Zoo#ROS)
- Jetson Zoo provides multiple docker containers for specific purposes such as using Tensor Flow, Ros2, etc.
- ready-to-use containers and Dockerfiles for Jetson and JetPack on the jetson-containers [GitHub repo](https://github.com/dusty-nv/jetson-containers)

#### 2. Download and Run the Docker Container:
- Follow the instructions provided in the Jetson Zoo or the GitHub repo to download and run the Docker container.
- Ensure:  you allow the container to be persistent by removing the ‘-rf’ flag from the docker run command. This prevents the container from being removed after it stops running.
  
#### 3. Once inside the container check if it has access to the GPU by using :
  
  `Nvidia-smi`
  If nvidia-smi is not available (some jetsons can't use nvidia-smi), you can check the CUDA version using:
  
  `Nvcc –version` 
  

#### 4. Some links lead to a docker hub link containing multiple images for a specific system
   - Downloading images from docker hub directly is easier	


