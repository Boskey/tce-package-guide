Tanzu Community Edition uses a Global Repository to Store Packages.
Users can point the `Tanzu CLI` to a specific Repository and a list of Packages referred in that repository are available for Installing on the Kubernetes Cluster.

The `Package Manager` uses `kapp-controller` , part of `Carvel` tools to manage Packages.

![Tanzu Community Edition Package Management](/workshop/content/images/tce-package-manager.png)

There are different versions of Package Repository,like, `stable`, `latest` etc. The `stable` version has the most latest version of each package available for install.

Let's add a Package Repository

```execute
tanzu package repository add tce-repo --url projects.registry.vmware.com/tce/main:stable --namespace {{session_namespace}}
```

This command tells `Tanzu CLI` where the package Repository is via the `URL` parameter. Once the Package Repository is added, it may take a minute to reconcile meta-data.



List the Packages Repositories added to `Tanzu CLI`

**NOTE: Give the above command ~30 seconds to reconcile and make sure the status says `Reconcile Succeeded` before proceeding to further steps.**

```execute
tanzu package repository list --namespace {{session_namespace}}
```
Take a look at the packages available via Repository, give the above command ~30 seconds to reconcile and make sure the status says `Reconcile Succeeded` 


```execute
tanzu package available list --namespace {{session_namespace}}
```

The above command will show all the packages available to install/configure/upgrade.
