Tanzu Package manager also provides a way to configure and update packages.

Each Package has a default set of configuration variation/values that are used when nothing is explicitly specified.

To list the various options available to configure a package and to see the default values we can use `values-schema` flag.

```execute
tanzu package available get  cert-manager.community.tanzu.vmware.com/1.3.1  --namespace {{session_namespace}} --values-schema
```

The above command will provide you with a list of configuration parameters that can be changed or updated with `tanzu` CLI.

you can update a config or change one by listing the configuration values in a YAML file and supplying it.

Let's update the application `Cert-Manager`

Let's look at the version of Cert-Manager we just installed. 

```execute
tanzu package installed list --namespace {{session_namespace}}
```
The current version of cert-manager is at `1.3.1`

Let's take a look at the available versions of Cert-Manager

```execute
tanzu package available list cert-manager.community.tanzu.vmware.com --namespace {{session_namespace}}
```

You will notice that Cert-manger has more recent versions available to upgrade.
Let's upgrade cert-manger ro version `1.5.1` from `1.3.1`

```execute
tanzu package installed update  cert-manager --version 1.5.1 --namespace {{session_namespace}} --wait=false
```

This would have updated cert-manager to version `1.5.1`. Let's confirm

```execute
tanzu package installed list --namespace {{session_namespace}}
```

