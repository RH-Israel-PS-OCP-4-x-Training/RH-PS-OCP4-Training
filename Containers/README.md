#  Containers course

# Containers concepts

**<span style="text-decoration:underline;">Deliveries:</span>**


* Difference between a container and a vm
* Are containers as isolated as vms
    * Hypervisor
    * Cgroup
    * namespace
* When will I want to use
    * vm
    * container

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://rancher.com/blog/2019/an-introduction-to-containers](https://rancher.com/blog/2019/an-introduction-to-containers)
* [https://www.cio.com/article/2924995/what-are-containers-and-why-do-you-need-them.html](https://www.cio.com/article/2924995/what-are-containers-and-why-do-you-need-them.html)
* [https://www.redhat.com/en/topics/containers/whats-a-linux-container](https://www.redhat.com/en/topics/containers/whats-a-linux-container)
* [https://www.redhat.com/en/topics/containers](https://www.redhat.com/en/topics/containers)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 4h
* Frontal



# The Dockerfile and building images

**<span style="text-decoration:underline;">Deliveries:</span>**



* Dockerfile options
* Build an image from a dockerfile

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://docs.docker.com/develop/develop-images/dockerfile_best-practices/](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2h

**<span style="text-decoration:underline;">Drill:</span>**



* Perform the following: [https://docs.docker.com/get-started/02_our_app/](https://docs.docker.com/get-started/02_our_app/)

# Docker container tools familiarity

**<span style="text-decoration:underline;">Deliveries:</span>**



* What is Docker
* Concepts:
    * Dockerfile
    * Base image
    * Entrypoint
    * CMD
* Docker commands (briefly):
    * ps
    * images
    * Run
    * Exec
    * Logs
    * Attach
    * Commit
    * pull
    * push
    * build
    * start
    * stop
    * inspect
    * info
    * save
    * load
    * Tag
    * login

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://docs.docker.com/get-started/overview/](https://docs.docker.com/get-started/overview/)
* [https://developers.redhat.com/blog/2021/01/11/getting-started-with-buildah/](https://developers.redhat.com/blog/2021/01/11/getting-started-with-buildah/)
* [https://goinbigdata.com/docker-run-vs-cmd-vs-entrypoint/#:~:text=ENTRYPOINT%20instruction%20allows%20you%20to,runs%20with%20command%20line%20parameters](https://goinbigdata.com/docker-run-vs-cmd-vs-entrypoint/#:~:text=ENTRYPOINT%20instruction%20allows%20you%20to,runs%20with%20command%20line%20parameters)
* [https://medium.com/analytics-vidhya/docker-practical-guide-421507289b13](https://medium.com/analytics-vidhya/docker-practical-guide-421507289b13)
* [https://docker-curriculum.com/](https://docker-curriculum.com/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 4.5h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**



* Build a docker container running apache on centos7 base image running a hello-world (customize as you will) page as a home page
* Save the image to file
* Copy and import the image to a new computer and run it on the second computer

# container storage

**<span style="text-decoration:underline;">Deliveries:</span>**
 * Where are files really saved when they are in a docker container.
 * What happens to files when a container is stopped, what happens when it is removed.
 * Volumes vs Mounts

 **<span style="text-decoration:underline;">Reading materials:</span>**
* [https://argus-sec.com/docker-networking-behind-the-scenes/](https://argus-sec.com/docker-networking-behind-the-scenes/)
* [https://docs.docker.com/network/](https://docs.docker.com/network/)


**<span style="text-decoration:underline;">Timing:</span>**
* DIY: 2h
* Frontal


# container networking

**<span style="text-decoration:underline;">Deliveries:</span>**
 * Familiarity with networking concept inside container
 * Familiarity with different types of network drivers
 * read only about bridge, host and none networks

 **<span style="text-decoration:underline;">Reading materials:</span>**
* [https://argus-sec.com/docker-networking-behind-the-scenes/](https://argus-sec.com/docker-networking-behind-the-scenes/)
* [https://docs.docker.com/network/](https://docs.docker.com/network/)


**<span style="text-decoration:underline;">Timing:</span>**
* DIY: 2h
* Frontal


# Tagging standards

**<span style="text-decoration:underline;">Deliveries:</span>**



* Tagging standards

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://docs.docker.com/engine/reference/commandline/tag/](https://docs.docker.com/engine/reference/commandline/tag/)
* [https://stevelasker.blog/2018/03/01/docker-tagging-best-practices-for-tagging-and-versioning-docker-images/](https://stevelasker.blog/2018/03/01/docker-tagging-best-practices-for-tagging-and-versioning-docker-images/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 2h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**



* Build an image
* Tag image as latest
* Tag image as v1
* Tag image as v2
* Push all images to repository (remote)


# OCI

**<span style="text-decoration:underline;">Deliveries:</span>**

* Why is there docker and docker-ce, what's the difference?
* What is OCI?
* Docker vs Podman
* Docker vs Buildah


**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://cri-o.io/](https://cri-o.io/)
* [http://docs.podman.io/en/latest/Commands.html](http://docs.podman.io/en/latest/Commands.html)
* [https://www.redhat.com/en/blog/red-hat-openshift-container-platform-4-now-defaults-cri-o-underlying-container-engine](https://www.redhat.com/en/blog/red-hat-openshift-container-platform-4-now-defaults-cri-o-underlying-container-engine)
* [https://www.openshift.com/blog/crictl-vs-podman](https://www.openshift.com/blog/crictl-vs-podman)
* [https://kubernetes.io/docs/tasks/debug-application-cluster/crictl/](https://kubernetes.io/docs/tasks/debug-application-cluster/crictl/)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 3h
* Frontal

# Nexus Container registry

**<span style="text-decoration:underline;">Deliveries:</span>**


* What are container registries
* Familiarize with nexus web-ui and functionality


**<span style="text-decoration:underline;">Reading materials:</span>**


* **[https://cloud.google.com/container-registry/docs/overview](https://cloud.google.com/container-registry/docs/overview)**
* **[https://hub.docker.com/r/sonatype/nexus3/](https://hub.docker.com/r/sonatype/nexus3/)**
* **[https://help.sonatype.com/repomanager3/user-interface](https://help.sonatype.com/repomanager3/user-interface)**

**<span style="text-decoration:underline;">Timing:</span>**

* DIY: 4h

**<span style="text-decoration:underline;">Drill:</span>**

* Install a nexus registry on your local machine
* Try different options inside nexus
* Push image to nexus (locally)


# skopeo

**<span style="text-decoration:underline;">Deliveries:</span>**


* skopeo
    * Copy
    * Delete
    * Inspect
    * Sync
    * Login
    * logout

**<span style="text-decoration:underline;">Reading materials:</span>**


* [https://www.redhat.com/en/blog/skopeo-10-released](https://www.redhat.com/en/blog/skopeo-10-released)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 1.5h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**

* Copy a container image between 2 registries

# Container image layers

**<span style="text-decoration:underline;">Deliveries:</span>**

* Understand what container layers are
* Understand the container overlayfs
* Understand what container layers are
* Scretch container
* Multistage build

**<span style="text-decoration:underline;">Reading materials:</span>**



* [https://jvns.ca/blog/2019/11/18/how-containers-work--overlayfs/](https://jvns.ca/blog/2019/11/18/how-containers-work--overlayfs/)
* [https://docs.docker.com/storage/storagedriver/overlayfs-driver/#:~:text=OverlayFS%20is%20a%20modern%20union,newer%20and%20more%20stable%20overlay2%20.](https://docs.docker.com/storage/storagedriver/overlayfs-driver/#:~:text=OverlayFS%20is%20a%20modern%20union,newer%20and%20more%20stable%20overlay2%20.)

**<span style="text-decoration:underline;">Timing:</span>**



* DIY: 3h
* Frontal

**<span style="text-decoration:underline;">Drill:</span>**

* Download the attached Dockerfile
* Fix it so it would still work, follow the best practices and have the smallest size possible.
* *DO NOT SEARCH FOR THE ORIGINAL DOCKERFILE!*



# Final Drill
* Install a local confluence
* Connect it to external db
* Reverse proxy without tls
    * Explain what a reverse proxy is

**<span style="text-decoration:underline;">Reading materials:</span>**

* [https://www.freecodecamp.org/news/docker-nginx-letsencrypt-easy-secure-reverse-proxy-40165ba3aee2/](https://www.freecodecamp.org/news/docker-nginx-letsencrypt-easy-secure-reverse-proxy-40165ba3aee2/)
