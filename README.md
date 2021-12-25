# helm-2-podman
repo to demo piping helm output to podman

This project takes image and app values defined in `values.yaml` and applys it to a pod definition.
The pod defintion can then be passed to podman to create a running pod.

Currently it defines an nginx instance


### run

With helm and podman installed 

```
git clone https://github.com/No9/helm-2-podman
cd helm-2-podman
helm template . | podman play kube -
```

### stop and delete pod 

```
podman pod stop nginx-pod
podman pod rm nginx-pod
```