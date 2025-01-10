export GH_USERNAME='Random-Dump'

export GITHUB_TOKEN=
export GITHUB_IMAGE_NAME=hello-world
export GITHUB_VER=1.0.0

echo $GITHUB_TOKEN | docker login ghcr.io -u $GITHUB_USER --password-stdin 

export TAG_NAME=ghcr.io/$GITHUB_USER/$GITHUB_IMAGE_NAME:1.0.0

echo $GITHUB_TOKEN | docker login ghcr.io -u $GITHUB_USER --password-stdin 

docker tag hello-world:latest $TAG_NAME

docker push $TAG_NAME

LABEL org.opencontainers.image.source https://github.com/OWNER/REPO