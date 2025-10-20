# Usage

The rapidsai/base image starts with an ipython shell⁠ by default.

The rapidsai/notebooks image starts with the JupyterLab notebook server⁠ by default.

## Container Ports

rapidsai/notebooks exposes port 8888 for the JupyterLab notebook server⁠.

## Environment Variables

The following environment variables can be passed to the docker run commands:

EXTRA_CONDA_PACKAGES - used to install additional conda packages in the container. Use a space separated list of values
CONDA_TIMEOUT - how long (in seconds) the conda command should wait before exiting
EXTRA_PIP_PACKAGES - used to install additional pip packages in the container. Use a space separated list of values
PIP_TIMEOUT - how long (in seconds) the pip command should wait before exiting
Example:

docker run \
 --rm \
 -it \
 --pull always \
 --gpus all \
 --shm-size=1g --ulimit memlock=-1 --ulimit stack=67108864 \
 -e EXTRA_CONDA_PACKAGES="jq" \
 -e EXTRA_PIP_PACKAGES="beautifulsoup4" \
 -p 8888:8888 \
 rapidsai/notebooks:25.10a-cuda13.0-py3.13
