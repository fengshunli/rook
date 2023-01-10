# Glossary

## Ceph

Ceph is a distributed network storage and file system with distributed metadata management and POSIX semantics. See also the [Ceph Glossary](https://docs.ceph.com/en/latest/glossary/) for more definitions.

### MON

Ceph Monitor is a daemon that maintains a map of the state of the cluster. This “cluster state” includes the monitor map, the manager map, the OSD map, and the CRUSH map. A Ceph cluster must contain a minimum of three running monitors in order to be both redundant and highly-available. Ceph monitors and the nodes on which they run are often referred to as “mon”s.

### MGR

The Ceph manager software, which collects all the state from the whole cluster in one place.

### MDS

The Ceph MetaData Server daemon. Also referred to as “ceph-mds”. The Ceph metadata server daemon must be running in any Ceph cluster that runs the CephFS file system. The MDS stores all filesystem metadata.

### OSD

Ceph Object Storage Daemon. The Ceph OSD software, which interacts with logical disks.

### RBD

The block storage component of Ceph. Also called "RADOS Block Device". It's a software instrument that orchestrates the storage of block-based data in Ceph.

### RGW

RADOS Gate Way. The component of Ceph that provides a gateway to both the Amazon S3 RESTful API and the OpenStack Swift API.

## Kubernetes

Kubernetes, also known as K8s, is an open-source system for automating deployment, scaling, and management of containerized applications. Here are some of the important terms from kubernetes perspective: 

* CSI
* CustomResourceDefinition (CRDs)
* Deployment
* DaemonSet
* Finalizer
* Node affinity
* nodeSelector
* Storage classes
* Toleration
* Volume

For further information see also the [Kubernetes Glossary](https://kubernetes.io/docs/reference/glossary) for more definitions.

### Ceph CSI

Ceph CSI plugins implement an interface between a CSI-enabled Container Orchestrator (CO) and Ceph clusters. For further information, please check out [CSI Driver documentation](https://rook.io/docs/rook/latest/Storage-Configuration/Ceph-CSI/ceph-csi-drivers/).

### Krew Plugin

The [Rook Krew plugin](https://rook.io/docs/rook/latest/Troubleshooting/krew-plugin/) is a tool to help troubleshoot your Rook cluster.

### OpenShift

OpenShift Container Platform is a cloud-based Kubernetes container platform. The foundation of OpenShift Container Platform is based on Kubernetes and therefore shares the same technology.

### Object Bucket Claim (OBC)

An Object Bucket Claim (OBC) is custom resource which requests a bucket (new or existing). For further reference please refer to [OBC Custom Resource](https://rook.io/docs/rook/latest/Storage-Configuration/Object-Storage-RGW/ceph-object-bucket-claim/).

### Object Bucket (OB)

An Object Bucket (OB) is a custom resource automatically generated when a bucket is provisioned. It is a global resource, typically not visible to non-admin users, and contains information specific to the bucket.

### Toolbox

The [Rook toolbox](https://rook.io/docs/rook/latest/Troubleshooting/ceph-toolbox/) is a container with common tools used for rook debugging and testing.

## Rook CRDs
### CephCluster CRDs

Rook allows creation and customization of storage clusters through the custom resource definitions (CRDs). For more information about the different modes of creation of clusters, refer our [documentation](https://rook.io/docs/rook/latest/CRDs/Cluster/ceph-cluster-crd/).

### Host Storage Cluster

A [host storage cluster](https://rook.io/docs/rook/latest/CRDs/Cluster/host-cluster/) is one where Rook configures Ceph to store data directly on the host.

### PVC Storage Cluster

In a [PVC-based cluster](https://rook.io/docs/rook/latest/CRDs/Cluster/pvc-cluster/), the Ceph persistent data is stored on volumes requested from a storage class of your choice.

### Stretch Storage Cluster

For environments that only have two failure domains available where data can be replicated, consider the case where one failure domain is down and the data is still fully available in the remaining failure domain. To support this scenario, Ceph has integrated support for [stretch clusters](https://rook.io/docs/rook/latest/CRDs/Cluster/stretch-cluster/).

### External Storage Cluster

An [external cluster](https://rook.io/docs/rook/latest/CRDs/Cluster/external-cluster/) is a Ceph configuration that is managed outside of the local K8s cluster.

### CephBlockPool CRD

Rook allows creation and customization of storage pools through the custom resource definitions (CRDs). The following settings are available for pools. For more information and examples refer this [documentation](https://rook.io/docs/rook/latest/CRDs/Block-Storage/ceph-block-pool-crd/).

### CephRBDMirror CRD

Rook allows creation and updating rbd-mirror daemon(s) through the custom resource definitions (CRDs). Here's an [example](https://rook.io/docs/rook/latest/CRDs/Block-Storage/ceph-rbd-mirror-crd/#creating-daemons) for the same.

### CephFilesystem CRD

Rook allows creation and customization of shared filesystems through the custom resource definitions (CRDs). Check out the examples [here](https://rook.io/docs/rook/latest/CRDs/Shared-Filesystem/ceph-filesystem-crd/#examples).

### CephFilesystemMirror CRD

Rook allows [creation](https://rook.io/docs/rook/latest/CRDs/Shared-Filesystem/ceph-fs-mirror-crd/#creating-daemon) and updating the Ceph fs-mirror daemon through the custom resource definitions (CRDs).

### CephObjectStore CRD

Rook allows [creation](https://rook.io/docs/rook/latest/CRDs/Object-Storage/ceph-object-store-crd/#example) and customization of object stores through the custom resource definitions (CRDs).

### CephClient CRD

Rook allows [creation](https://rook.io/docs/rook/latest/CRDs/ceph-client-crd/) and updating clients through the custom resource definitions (CRDs).

### CephNFS CRD

Rook allows exporting NFS shares of a CephFilesystem or CephObjectStore through the CephNFS custom resource definition. For further information please refer to the example [here](https://rook.io/docs/rook/latest/CRDs/ceph-nfs-crd/#example).

