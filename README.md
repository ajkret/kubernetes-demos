# kubernetes-demos

Demos from Kubernetes Deployment / Services scripts based on DevOpsPro / KubeDev course

## Using the internal application

To use the service running on NodePort mode, type:

    curl http://<k8s host>:<nodeport port>/temperatura/fahrenheitparacelsius/100

Where **nodeport port** can be obtained with a simple:

    kubectl get services -o wide

To use the service running on ClusterIp mode, create a temporary Pod, then use the curl command above with one of the nodes:

    run -i -tty --image kubedevio/ubuntu-curl ping-test --rm --restart=Never /bin/bash

Any image with **curl** will do. Obtain the available IP for the service with:

    kubectl get service conversion-cip -o wide







