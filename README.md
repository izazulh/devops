### command to build image using docker and pushing it to ecr
service=gateway && hash="$(git rev-parse --short HEAD)" && \
docker build --network=host -t 147466076004.dkr.ecr.ap-south-1.amazonaws.com/staging/$service:$hash . && \
docker push 147466076004.dkr.ecr.ap-south-1.amazonaws.com/staging/$service:$hash
