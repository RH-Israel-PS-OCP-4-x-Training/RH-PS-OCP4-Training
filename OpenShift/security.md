### lets start from Linux :) --> SELinux

- Everything in the operating system has a label
- Policy defines the interaction between a labeled process and labeled resources
- Policy comes with the distribution but you can add your own
- Policy is enforced by Kernel
- Enforcement is turned on by default
- Systems with SELinux enabled are less susceptible (e.g. container breakouts)
- Namespaces - isolation primitives

## Use OpenShift Security Context Constraints to manage these controls

- Allow administrators to control permissions for pods
- Restricted SCC is granted to all users
- By default, no containers can run as root
- Admin can grant access to privileged SCC
- Custom SCCs can be created

To view the existing SCC: `oc describe scc`


## Certificates and Certificate Management

<img width="145" alt="image" src="https://user-images.githubusercontent.com/100561043/167843159-885ce328-8426-4880-9064-4fcf90a919d2.png">

- OpenShift provides its own internal CA
- __Certificates__ are used to provide secure connections to:
  - master (APIs) and nodes
  - Ingress controller and registry
  - etcd
- Certificate rotation is automated
- Optionally configure external endpoints to use custom certificates

## Service Certificates

<img width="851" alt="image" src="https://user-images.githubusercontent.com/100561043/167843368-74de0fd0-3453-41c3-82f9-62cee5c5c5b2.png">

Users create a `service` and then annotate with service.alpha.openshift.io/serving-cert-my -- the service serving cert signer then creates a keypair and puts it into a secret

Users create a ConfigMap and then annotate it with service.beta.openshift.io/inject-cabundle="true" -- the configmap cabundle injector then adds the CA bundle to the configmap

Users define pods, deployments, etc. and mount the secret and configmap as needed so that their service now has full TLS provided by the built-in CA, and other services that add the CA bundle can consume this service and trust its certificates
Note that this overlaps with Service Mesh’s ability to provide transparent mutual TLS -- use one or the other, not both.

## The Service CA Operator

- The Service Certificate Authority (CA) can sign server certificates for services running in the OpenShift cluster. 
- The service-ca operator manages 3 controllers
  - service-ca controller
  - configmap-cabundle-injector controller
  - apiservice-cabundle-injector controller
 
 
