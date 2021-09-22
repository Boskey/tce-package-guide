Once we have `Package Repository` added to Tanzu CLI, we can list the avaialble packages to install.

Let's install `Cert-Manager`, package  that provides certificate management for applications on the Cluster. To install Cert-Manager we first need to fetch the version available.

List the packages available to get the Cert-Manager Package URL

```execute
tanzu package available list --namespace {{session_namespace}}
```

Fetch the version of the `Cert-Manager` available to install.

```execute
tanzu package available list cert-manager.community.tanzu.vmware.com  --namespace {{session_namespace}}
```

Install Cert-Manager

```execute
tanzu package install cert-manager --package-name cert-manager.community.tanzu.vmware.com --namespace {{session_namespace}}  --version 1.3.1 --wait=false

The above command would have installed `Cert-Manager`

Let's list the packages installed.

```execute
tanzu package installed list --namespace {{session_namespace}}
```
NOTE: You might see an error message saying `Reconcile Failed...` . This is because there are other users going through the tutorial and might have installed another version of cert-manager on the cluster.

