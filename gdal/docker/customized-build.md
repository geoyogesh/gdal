cd gdal\gdal\docker\ubuntu-small

docker login
$DOCKER_ACC="geoyogesh"
$DOCKER_REPO="gdal"
$IMG_TAG_LATEST="latest"
$IMG_TAG="3.1.3"
docker build -t geoyogesh/gdal:latest .
docker push geoyogesh/gdal:latest
docker image tag $DOCKER_ACC/$DOCKER_REPO:$IMG_TAG_LATEST $DOCKER_ACC/$DOCKER_REPO:$IMG_TAG
docker push geoyogesh/gdal:3.1.3
