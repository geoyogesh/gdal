
- get access token
``` bash
aws ecr-public get-login-password --region us-east-1 | docker login --username AWS --password-stdin public.ecr.aws/y9i8a9u6

```

docker build -t p4p/gdal .

docker tag p4p/gdal:latest public.ecr.aws/y9i8a9u6/p4p/gdal:latest
docker tag p4p/gdal:latest public.ecr.aws/y9i8a9u6/p4p/gdal:3.3.0

docker push public.ecr.aws/y9i8a9u6/p4p/gdal:latest
docker push public.ecr.aws/y9i8a9u6/p4p/gdal:3.3.0
