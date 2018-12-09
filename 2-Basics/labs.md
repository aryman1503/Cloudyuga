### 3. How to start a pod ?

With the `rkt run` command we can start a pod.


```command
rkt  run --insecure-options=image docker://nginx
```
```output
Downloading sha256:046e44ee605 [=============================]     193 B / 193 B
Downloading sha256:75a822cd788 [=============================] 51.4 MB / 51.4 MB
Downloading sha256:0aefb9dc4a5 [=============================] 20.2 MB / 20.2 MB
```

`nginx` would start running in the foreground, which would our terminal. To do other operation we need to start another session to the host.

### 4. How to list the rkt pods ?
With `rkt list` command we can list the pod.


```command
rkt list
```
```output
UUID            APP     IMAGE NAME                                      STATE   CREATED         STARTED         NETWORKS
29614ed8        nginx   registry-1.docker.io/library/nginx:latest       running 3 minutes ago   3 minutes ago   default:ip4=172.16.28.2
```

Each pod gets a unique UUID which is referred by `UUID` field. By default `APP` name set the image name which means multiple pods can have same `APP` name.

### 5. How to set the custom `APP` name for a pod  ?
We can give custom `APP` name with `--name` option to `rkt run` command as follows:-
``` command
rkt --insecure-options=image run docker://busybox --name=busybox1
```

- List the containers.

```command
rkt list
```
