# Metal³

The Metal³ project (pronounced: "Metal Kubed") provides components for bare
metal host management with Kubernetes. You can enrol your bare metal machines,
provision operating system images, and then, if you like, deploy Kubernetes
clusters to them. From there, operating and upgrading your Kubernetes clusters
can be handled by Metal³. Moreover, Metal³ is itself a Kubernetes application,
so it runs on Kubernetes, and uses Kubernetes resources and APIs as its
interface.

Metal³ is one of the providers for the Kubernetes sub-project [Cluster
API](https://github.com/kubernetes-sigs/cluster-api). Cluster API provides
infrastructure agnostic Kubernetes lifecycle management, and Metal³ brings the
bare metal implementation.

This is paired with one of the components from the OpenStack ecosystem,
[Ironic](https://ironicbaremetal.org/) for booting and installing machines.
Metal³ handles the installation of Ironic as a standalone component (there's no
need to bring along the rest of OpenStack). Ironic is supported by a mature
community of hardware vendors and supports a wide range of bare metal
management protocols which are continuously tested on a variety of hardware.
Backed by Ironic, Metal³ can provision machines, no matter the brand of
hardware.

In summary, you can write Kubernetes manifests representing your hardware and
your desired Kubernetes cluster layout. Then Metal³ can:

* Discover your hardware inventory
* Configure BIOS and RAID settings on your hosts
* Optionally clean a host's disks as part of provisioning
* Install and boot an operating system image of your choice
* Deploy Kubernetes
* Upgrade Kubernetes or the operating system in your clusters with a
  non-disruptive rolling strategy
* Automatically remediate failed nodes by rebooting them and removing them from
  the cluster if necessary

You can even deploy Metal³ to your clusters so that they can manage other
clusters using Metal³...

Metal³ is [open-source](https://github.com/metal3-io) and welcomes community
contributions. The community meets at the following venues:

* \#cluster-api-baremetal on [Kubernetes Slack](https://slack.k8s.io/)
* Metal³ development [mailing list](https://groups.google.com/g/metal3-dev)
* From the mailing list, you'll also be able to find the details of a weekly
  Zoom community call on Wednesdays at 14:00 GMT
* Roadmap discussion: https://docs.google.com/document/d/1Exm5k6JB2JlD9_FOaM68R2ASHi7ZsryF_xEqLG1j4zA
* Roadmap GitHub project: https://github.com/orgs/metal3-io/projects/8
* Feel free to add your organization as an adopter to  https://github.com/metal3-io/community/blob/main/ADOPTERS.md 
* Flake tracker: https://github.com/orgs/metal3-io/projects/4
* CLO monitor: https://clomonitor.io/projects/cncf/metal3-io 
* Dev stats: https://metal3.devstats.cncf.io/d/8/dashboards?orgId=1&from=now-1y&to=now-1h&editPanel=2 
* Container images (Quay): https://quay.io/organization/metal3-io
* Jenkins periodics: https://jenkins.nordix.org/view/Metal3%20Periodic/ 
* Prow: https://prow.apps.test.metal3.io/
* Security processes and volnerability disclousure info: https://book.metal3.io/security_policy
* Community, governance and contribution policies can be found here: https://github.com/metal3-io/community
* User guide: https://book.metal3.io/introduction
* Architectural design proposals: https://github.com/metal3-io/metal3-docs/tree/main/design
