docker login

docker tag istio/examples-bookinfo-productpage-v1:1.20.3 tunnyeinmua/bookinfo-product-page:1.20.3

docker push tunnyeinmua/bookinfo-product-page:1.20.3


#docker pull
docker pull istio/examples-bookinfo-details-v1:1.20.3

docker tag istio/examples-bookinfo-details-v1:1.20.3 tunnyeinmua/bookinfo-details-v1:1.20.3

docker push tunnyeinmua/bookinfo-details-v1:1.20.3

docker pull istio/examples-bookinfo-ratings-v1:1.20.3

docker tag istio/examples-bookinfo-ratings-v1:1.20.3 tunnyeinmua/bookinfo-ratings-v1:1.20.3
docker push tunnyeinmua/bookinfo-ratings-v1:1.20.3


docker pull istio/examples-bookinfo-reviews-v1:1.20.3
docker tag istio/examples-bookinfo-reviews-v1:1.20.3 tunnyeinmua/bookinfo-reviews-v1:1.20.3
docker push tunnyeinmua/bookinfo-reviews-v1:1.20.3


docker pull istio/examples-bookinfo-reviews-v2:1.20.3
docker tag istio/examples-bookinfo-reviews-v2:1.20.3 tunnyeinmua/bookinfo-reviews-v2:1.20.3
docker push tunnyeinmua/bookinfo-reviews-v2:1.20.3

docker pull istio/examples-bookinfo-reviews-v3:1.20.3
docker tag istio/examples-bookinfo-reviews-v3:1.20.3 tunnyeinmua/bookinfo-reviews-v3:1.20.3
docker push tunnyeinmua/bookinfo-reviews-v3:1.20.3



aws ecr get-login-password --region ap-southeast-1 --profile master-console-admin | docker login --username AWS --password-stdin 767397836388.dkr.ecr.ap-southeast-1.amazonaws.com


/home/tunnyein/Pictures/Screenshots/Screenshot from 2025-05-11 16-07-53.png


docker pull 767397836388.dkr.ecr.ap-southeast-1.amazonaws.com/docker-hub-a887/tunnyeinmua/bookinfo-product-page:1.20.3

tunnyeinmua/bookinfo-details-v1:1.20.3
docker pull 767397836388.dkr.ecr.ap-southeast-1.amazonaws.com/docker-hub-a887/tunnyeinmua/bookinfo-details-v1:1.20.3


docker pull 767397836388.dkr.ecr.ap-southeast-1.amazonaws.com/docker-hub-a887/tunnyeinmua/bookinfo-ratings-v1:1.20.3



kubectl create secret generic regcred \
  --type=kubernetes.io/dockerconfigjson \
  --from-file=.dockerconfigjson=$HOME/.docker/config.json \
  -n book-info

  kubectl create secret docker-registry my-secret --from-file=$HOME/.docker/config.json
