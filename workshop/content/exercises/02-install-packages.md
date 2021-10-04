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

To install Cert-Manager, run the following commad. 
Note: We are not going to run the below command since this is a shared cluster and Cert-Manger can be installed only once. 

```
tanzu package install cert-manager --package-name cert-manager.community.tanzu.vmware.com  --version 1.3.1 --wait=false
```

The above command was used to install `Cert-Manager`

Let's list the packages installed.

```execute
tanzu package installed list
```

You can similarly select a package from the available list and use `tanzu package install` command to install additional packages.
