# Head-less-service

A headless service in Kubernetes is a service with clusterIP set to None, which does not provide load balancing. Instead, it returns the individual pod IPs via DNS, allowing direct communication with pods, typically used for stateful applications.

# Command for DNS check
kubectl run -it --rm --restart=Never --image=busybox dns-test -- nslookup mysql-statefulset-0.my-db-headless-service.default.svc.cluster.local
