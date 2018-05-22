# Run OpenShift using Docker

docker run -d --name "openshift-$RANDOM" --net=host --privileged -v /var/run/docker.sock:/var/run/docker.sock openshift/origin start

--> https://localhost:8443
