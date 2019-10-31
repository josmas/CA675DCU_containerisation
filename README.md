# Containerisation Demo - CA675 DCU Week 6
A small ML program run directly through a container

# Step 1: clone the repo
Clone this repo into a VM with docker installed:

`git clone https://github.com/josmas/CA675DCU_containerisation.git`

# Step 2: Build the image
`docker build -t jos/classification:1 .`

Note that you can modify the name of the container as you see fit.

You can see your new image with `docker images`

# Step 3: Run the container
`docker run --rm --name class_1 jos/classification:1`

If you have modified the name of the container, you'll also have to modify the
invocation command.

# Step 4 (Optional)
You can run the container iteratively and connect to it through a shell with:
`docker run -it --name class_1 jos/classification:1 bash`

You can see your container running if you type `docker ps` from a second
terminal.

If you also map your local folder, you can run whatever python scripts you want
from the terminal. Look at the docs for Bind Mounts and Volumes from the Docker
site.

# References
The code in this repo is based on the article at: https://towardsdatascience.com/beginners-guide-to-data-science-python-docker-3181fd321a5c

Jos, Oct 2019
