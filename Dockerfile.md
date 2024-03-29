
**1. FROM**  
Specifies the base image from which you are building.
Example: `FROM ubuntu:latest` (Uses the latest Ubuntu image as the base)

**2. COPY**  
Copies files or directories from the host into the container's filesystem at a specified destination.
Example: `COPY . /app` (Copies all files from the current directory on the host into the `/app` directory in the container)

**3. ADD**  
Similar to COPY but with additional features like extracting files from URLs and unpacking TAR archives.
Example: `ADD https://example.com/archive.tar.gz /app` (Downloads and extracts `archive.tar.gz` from a URL into the `/app` directory in the container)

**4. RUN**  
Executes commands in the container's shell during the build process.
Example: `RUN apt-get update && apt-get install -y python3` (Updates package lists and installs Python 3 inside the container)

**5. CMD**  
Specifies the default command to run when the container starts.
Example: `CMD ["python3", "app.py"]` (Runs the `app.py` Python script when the container starts)

**6. WORKDIR**  
Sets the working directory for subsequent instructions.
Example: `WORKDIR /app` (Sets the `/app` directory as the working directory)

**7. ENV**  
Sets environment variables in the container.
Example: `ENV APP_PORT=8080` (Sets an environment variable `APP_PORT` with the value `8080`)

**8. EXPOSE**  
Informs Docker that the container listens on specific network ports at runtime.
Example: `EXPOSE 80` (Informs Docker that the container listens on port `80`)

**9. VOLUME**  
Creates a mount point for a volume to be used with other containers or by the host.
Example: `VOLUME /var/data` (Creates a volume named `/var/data`)

**10. ENTRYPOINT**  
Configures the container to run as an executable.
Example: `ENTRYPOINT ["java", "-jar", "app.jar"]` (Specifies that `java -jar app.jar` is the default command to run when the container starts)

