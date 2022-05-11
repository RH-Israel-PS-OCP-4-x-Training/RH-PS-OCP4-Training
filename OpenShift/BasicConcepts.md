# Lets Learn Basic Concepts

OpenShift uses Podman on the bastion machine, so we will use podman as-well 

## what is `container`

The `container` is the smallest compute unit.
You can view the running containers with ```podman ps```

A container is created by a static build called `Image` that holds the binaries:


<img width="344" alt="image" src="https://user-images.githubusercontent.com/100561043/167797354-5c04ecd1-f915-4c09-a3c0-0388aacd8bdb.png">


On Openshift platform images are saved on a `Registry`:
A `registry` is an `hub` of images, and it can be localy in the cluster or outside the cluster, like `Quey` or `DockerHub`

https://hub.docker.com/
https://quay.io/

At the `registry` the images are saved with `tags` that represent the `version` of the binary.

<img width="600" alt="image" src="https://user-images.githubusercontent.com/100561043/167798887-27571b2b-ebe3-4a30-b74e-94018e615f29.png">

## POD

At openshit The smallest compute unit that can be defined, deployed, and managed is called - **`Pod`**
A `pod` wraps a `container` and provide:
- CPU
- Memory
- Network
- Storage

## ReplicaSet V.S ReplicationController

Both are used to manage and ensure a specified number of pods are running at any given time at the cluster.
But `ReplicationController` does not support set-based selector requirements, and `ReplicaSet` do.


## Deployments

are responsible to define how to roll out new versions of Pods

## Deployments V.S DeploymentConfig

| Deployments | DeploymentConfig |
| :---: | :---: |
| Deployments is driven by a controller manager | Use deployer pods for every new rollout |
| Deployments take availability over consistency The controller manager runs in high availability mode on masters and uses leader election algorithms to value availability over consistency | DeploymentConfigs prefer consistency If a node running a deployer pod goes down, it will not get replaced. The process waits until the node comes back online or is manually deleted  |
| Has an implicit ConfigChange trigger.  Every change in the deployment automatically triggers a new rollout | ConfigChange triggers are explicit |
| Do not yet support any lifecycle hooks | Support lifecycle hooks (pre, mid, post) |
| Rollback to the last ReplicatSet is not supported. | Support automatically rolling back to the last successfully deployed ReplicationController |

