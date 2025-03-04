# HA proxy example kubernetes

# Local test
kubectl port-forward svc/haproxy-service 8080:80
curl localhost:8080

# Config is in configmap

# HAproxy frontend is reachable from pods with cluster DNS
http://haproxy-service.default.svc.cluster.local:80
haproxy-service.default.svc.cluster.local

---> forwards to HAproxy backend
