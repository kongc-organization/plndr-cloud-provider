# plndr-cloud-provider
A bare metal cloud provider for Kubernetes


Configure Cloud Provider RBAC:

`k create -f https://raw.githubusercontent.com/plunder-app/plndr-cloud-provider/master/example/pod/rbac.yaml`

Deploy Cloud Provider:

**WARNING**

By default the VIP / Loadbalancer cidr is 192.168.0.80/30, to modify this download the manifest and edit the line before applying to the cluster.

`k create -f https://raw.githubusercontent.com/plunder-app/plndr-cloud-provider/master/example/pod/plndr-cloud-provider.yaml`

Configure `kube-vip` RBAC:

`k create -f https://raw.githubusercontent.com/plunder-app/kube-vip/master/example/pod/rbac.yaml`

Deploy Kube-VIP:

`k create -f https://raw.githubusercontent.com/plunder-app/kube-vip/master/example/pod/kube-vip.yaml`

Deploy starboard Daemonset:

`k create -f https://raw.githubusercontent.com/plunder-app/starboard/master/examples/daemonset/0.1.yaml`
