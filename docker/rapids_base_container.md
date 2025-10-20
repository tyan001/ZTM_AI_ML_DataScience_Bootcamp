Mounting files/folders to the locations specified below provide additional functionality for the images.

/home/rapids/environment.yml - a YAML file that contains a list of dependencies that will be installed by conda. The file should look like:
dependencies:

- beautifulsoup4
- jq
  Example:

docker run \
 --rm \
 -it \
 --pull always \
 --gpus all \
 --shm-size=1g --ulimit memlock=-1 --ulimit stack=67108864 \
 -v $(pwd)/environment.yml:/home/rapids/environment.yml \
 rapidsai/base:25.10a-cuda13.0-py3.13
