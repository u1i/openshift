# Run OpenShift using Docker

docker run -d --name "openshift-$RANDOM" --net=host --privileged -v /var/run/docker.sock:/var/run/docker.sock openshift/origin start

--> https://localhost:8443

# Get oc commandline tool

https://github.com/CCI-MOC/moc-public/wiki/Installing-the-oc-CLI-tool-of-OpenShift

# Commands
oc new-app https://github.com/u1i/openshift-python-bottle.git

oc expose svc/openshift-python-bottle

oc get pods

oc autoscale dc/openshift-python-bottle --min 3 --max 10 --cpu-percent=80

oc new-app u1ih/hello

oc expose svc/hello

oc delete all -l app=myapp

oc get route

oc describe limits resource-limits

## Trigger redeplyment

oc rollout latest dc/yoisho-atm
