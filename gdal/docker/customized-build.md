cd gdal\gdal\docker\alpine-normal

docker login
$DOCKER_ACC="geoyogesh"
$DOCKER_REPO="gdal"
$IMG_TAG_LATEST="alpine-normal-latest"
$IMG_TAG="alpine-normal-3.1.3"
docker build -t $DOCKER_ACC/$DOCKER_REPO:$IMG_TAG_LATEST .
docker push $DOCKER_ACC/$DOCKER_REPO:$IMG_TAG_LATEST
docker image tag $DOCKER_ACC/$DOCKER_REPO:$IMG_TAG_LATEST $DOCKER_ACC/$DOCKER_REPO:$IMG_TAG
docker push $DOCKER_ACC/$DOCKER_REPO:$IMG_TAG
