# helm-2-podman
repo to demo piping helm output to podman

This project takes image and app values defined in `values.yaml` and applys it to a pod definition.
Currently it defines an nginx instance

The pod defintion can then be passed to podman to create a running pod.

```
helm template . | podman play kube -
```

### stop and delete pod 

```
podman pod stop nginx-pod
podman pod rm nginx-pod
```