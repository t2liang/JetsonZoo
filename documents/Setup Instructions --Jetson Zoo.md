## Docker set-up
#### 1. Figure out what Development environment you need and then visit [Jetson Zoo](https://elinux.org/Jetson_Zoo#ROS)
- Jetson Zoo provides multiple docker containers for specific purposes such as using Tensor Flow, Ros2, etc.
- ready-to-use containers and Dockerfiles for Jetson and JetPack on the jetson-containers [GitHub repo](https://github.com/dusty-nv/jetson-containers)

#### 2. Once you find what you need, follow the instructions to download and run the container.
- Make sure you allow the container to be persistent by removing the ‘-rf’ flag from the docker run command
  
#### 3. Once inside the container check if it has access to the GPU by using :
  
  ```python
  Nvidia-smi
  Nvcc –version (some jetsons can't use nvidia-smi)
  ```

4. Some links lead to a docker hub link containing multiple images for a specific system
   - Downloading images from docker hub directly is easier	


