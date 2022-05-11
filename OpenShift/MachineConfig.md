## Machine Config Operator

The Machine Config Operator provides cluster-level configuration, enables rolling upgrades, and prevents drift between new and existing nodes. The MCO is the heart of what makes RHCOS a kube-native operating system

- OS configuration is stored and applied across the cluster via the Machine Config Operator.
- Subset of ignition modules applicable post provisioning
  - SSH keys
  - Files
  - systemd units
  - kernel arguments
- Standard k8s YAML/JSON manifests
- Desired state of nodes is checked/fixed regularly
- Can be paused to suspend operations

The Machine Config Operator is responsible for deployment of three primary operands
- the Machine Config Controller (MCC)
- the Machine Config Server (MCS) 
- the Machine Config Daemon (MCD)



### MachineConfig

` MachineConfig ` are rendered into a single config that targets a MachineConfigPool, or a group of systems. This is the job of the Machine Config Controller.
Default pools are: master & worker
Custom MachineConfigPools can be created as needed
Custom MachineConfigPools use inheritance to help scale

### MachineConfigPool

A MachineConfigPool has two things it targets -- relevant nodes, and relevant MachineConfig objects.
The MachineConfigPool has a nodeselector which determines which nodes the pool applies to.
The MachineConfigPool has a machineConfigSelector which determines which MachineConfigs belong / are relevant.


