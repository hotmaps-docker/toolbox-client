# HotMaps-toolbox-client Docker image

This Docker image offers a web server based on Nginx.

###Build and run:
### Build
To build this image from Dockerfile run this command in your Docker or Docker Toolbox shell:

`docker build -t hotmaps/toolbox .`

### Run

**Important:** Before running make sure you have a directory containing some code. This directory will be linked to the volume of the container. Here is the most basic file that needs to be in that directory*:

**index.html**


To create a container use this command*:

`docker run -d -v "`*absolute/path/to/your/code*`:/usr/share/nginx/html" -p 80:80 -it hotmaps/res-potential`

On Windows the absolute path to your code directory should be in the format */c/My-first-dir/my-second-dir/my-code-dir*

**Note that you can pull the image directly from the repository with this same command but make sure you have a "data" directory (linked to the volume -v) containing some working code (see example above).*

After successfuly running this command, open your web browser and go to `{ip-of-your-docker-host}:80`

If you don't know the IP address of your docker machine type `docker-machine ip` in your terminal.

## How to add your own application

To place your own code, go to the directory linked with your volume that your previously created (cf. Run) and place your own code there.


