## Basic Linux Security Concepts

> ### Files & Dir permissions #ToDO @barak

### SELinux
- Everything in the operating system has a label
- Policy defines the interaction between a labeled process and labeled resources
- Policy comes with the distribution but you can add your own
- Policy is enforced by Kernel
- Enforcement is turned on by default
- Systems with SELinux enabled are less susceptible (e.g. container breakouts)
- Namespaces - isolation primitives

> ### Capabilities #ToDO @barak

## SCC - OpenShift Security Context Constraints

- Allow administrators to control permissions for pods
- Restricted SCC is granted to all users **by default**
- By default, no container can run as root
- Admin can grant access to privileged SCC
- Custom SCCs can be created

To view the existing SCC: 
```bash
$ oc get scc
$ oc describe scc restricted
$ oc describe scc privileged
```


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
 
 
## Identity and Access Management

<img width="682" alt="image" src="https://user-images.githubusercontent.com/100561043/167845064-56a3abda-d49c-4bb1-af8c-06d42ca335cf.png">

OpenShift includes an OAuth server, which does three things: 
- Identifies the person requesting a token, using a configured identity provider
- Determines a mapping from that identity to an OpenShift user
- Issues an OAuth access token which authenticates that user to the API 


### Configuring an Identity provider

- Determines a mapping from that identity to an OpenShift user
  - Allows multiple identities to map to the same OpenShift user
  - Allows deconflicting between identity provider roles
- In many cases the credentials are validated against the identity provider directly (not necessarily given to the OAuth server)


## Fine-Grained RBAC

- Project scope & cluster scope available
- Matches request attributes (verb,object,etc)
- If no roles match, request is 
- denied ( deny by default )
- Operator- and user-level 
- roles are defined by default
- Custom roles are supported

In OpenShift we have a role based authorization component. 
There is a Project scope and a Cluster scope where either `RoleBindings` or `ClusterRolebindings` define the permissions a user will have once logged in. This role component matches attributes on the request like the verb on the objects for example  get projects or create pods. 
It matches those attributes to roles which have been grated to the requesting user. 
If no roles match the request is denied. 
By default everything is denied unless the role specifically allows it. Out of the box operator and user level roles are defined and custom roles are also supported. 	

 
 
