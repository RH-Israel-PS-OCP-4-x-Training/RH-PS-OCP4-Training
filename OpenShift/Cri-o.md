# Cri-o 

Please Read https://cri-o.io/
It contains much information about How Cri-o Works.

But TL;TR:

Cri-o is the Container engine that Openshift uses to manage it containers.
It runs on each worker and at the controlplane.

<img width="908" alt="image" src="https://user-images.githubusercontent.com/100561043/173797340-d8f8a1fc-51b6-42f2-b41b-33f76bd92847.png">

- Kubernetes contacts the kubelet to launch a pod.
- Pods are a kubernetes concept consisting of one or more containers sharing the same IPC, NET and PID namespaces and living in the same cgroup.
- The kubelet forwards the request to the CRI-O daemon VIA kubernetes CRI (Container runtime interface) to launch the new POD.
- CRI-O uses the containers/image library to pull the image from a container registry.
- The downloaded image is unpacked into the container’s root filesystems, stored in COW file systems, using containers/storage library.
- After the rootfs has been created for the container, CRI-O generates an OCI runtime specification json file describing how to run the container using the OCI Generate tools.
- CRI-O then launches an OCI Compatible Runtime using the specification to run the container proceses. The default OCI Runtime is runc.
- Each container is monitored by a separate conmon process. The conmon process holds the pty of the PID1 of the container process. It handles logging for the container and records the exit code for the container process.
- Networking for the pod is setup through use of CNI, so any CNI plugin can be used with CRI-O.
