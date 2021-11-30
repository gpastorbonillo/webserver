# webserver

I don't know what i´m doing.
Trying kubernetes out


HTML folder containing generated sample html content, dockerfile to build a local nginx image, docker-file to test it out. 

Webserver-pod.yml defines the pod, webserver-replicaset.yml defines it again, this time in HA. 

Webserver-lb-yml exposes the replica set through an allocated metal-lb owned IP, webserver-lvv2.yml creates the service but doesnt expose it outside the cluster

Webserver-ingress.yml exposes the replica set through nginx ingress controller, in two domain names, and exposes it outside thtough another metal-lb owned IP, wich then is exposed to the internet.

It presents certbot generated certs for both of them, wich are added manually as secrets. 

