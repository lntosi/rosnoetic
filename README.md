rosnoetic
=========

## How to build:

**Step 1:** After cloning this repository, give permissions to execute the file "ros_entrypoint.sh".
 
```shell
chmod +x ros_entrypoint.sh
```

**Step 2:** Build the Dockerfile to create an image with all the required dependencies named "rosnoetic".
 
```shell
docker build -t rosnoetic .
```

**Step 3:** Use this to run a container with a volume (delete --rm if you want to keep the container after quitting):

```shell
docker run -it --rm --name rosnoetic-container \
-v /<local path>/ROS:/<container path>/ROS \
rosnoetic
```
