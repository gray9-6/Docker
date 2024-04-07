# Docker

Here's a properly formatted guide on Docker basics, including commands and examples:

1. Check Docker Version:
   ```
   docker -v 
   ```

2. Pull an Image:
   ```
   docker pull image_name
   ```

   Example:
   ```
   docker pull openjdk
   ```

2.1 Pull Different Versions of the Same Image:
   ```
   docker pull image_name:tag
   ```

   Example:
   ```
   docker pull openjdk:18
   ```

3. Check Local Images:
   ```
   docker images
   ```

4. Search for an Image:
   ```
   docker search image_name
   ```

   Example:
   ```
   docker search MySQL
   ```

5. Run an Image:
   ```
   docker run image_name
   ```

   Example:
   ```
   docker run python
   ```

5.2 Check Running Containers:
   ```
   docker ps
   ```

6. Check All Containers:
   ```
   docker ps -a
   ```

7. Give a Name to Your Container and Start in Detached Mode:
   ```
   docker run --name container_name -d image_name
   ```

8. Interact with Docker:
   ```
   docker run --name container_name -it -d image_name
   ```

9. Enter a Running Container:
   ```
   docker exec -it container_id command
   ```

   Example:
   ```
   docker exec -it b441b2d83bb1 python3
   ```

10. Inspect Container Information:
    ```
    docker inspect container_id
    ```

    Example:
    ```
    docker inspect b441b2d83bb1
    ```

11. Stop a Container:
    ```
    docker stop container_name
    ```

12. Remove a Container:
    ```
    docker rm container_id
    ```

13. Remove Docker Images:
    ```
    docker rmi image_name
    ```

14. Restart a Container:
    ```
    docker restart container_name
    ```

15. Login to Docker:
    ```
    docker login
    ```

16. Create and Save an Edited Container Image:
    ```
    docker commit
    ```

17. Push Docker Image to Repository or Docker Hub:
    ```
    docker push
    ```

18. Copy a File from Docker Hub to Local System:
    ```
    docker cp
    ```

19. Check Container Logs:
    ```
    docker logs container_name
    ```

20. Manage Docker Volumes:
    ```
    docker volume
    ```

21. Logout from Docker Hub:
    ```
    docker logout
    ```

To create your Docker image:

1. Create a folder where you want to create the image and navigate to that path in the terminal.

2. Create a Dockerfile with no extension and add the following code:
   ```Dockerfile
   # Base image to use
   FROM ubuntu:latest

   # Maintainer information
   LABEL maintainer="ajay"

   # Commands to run when building the image
   RUN apt-get update

   # Default command to run when a container starts
   CMD [ "echo", "This is my first Ubuntu image" ]
   ```

3. Build the image using the command:
   ```
   docker build -t your-image-name .
   ```

This guide covers basic Docker commands and how to create your Docker image.
