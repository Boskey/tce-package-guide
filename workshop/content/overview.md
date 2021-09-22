Tanzu Community Edition enables the creation of modern application platforms. These platforms can be created on local laptops or various clouds/Infrastructure Environments. A platform deployed using tanzu Community edition provides a Kubernetes Run time, Tooling and additional repository of packages that can be installed/updated very easily.

This workshop we will focus on packages that can be installed using Tanzu Community Edition. 

Tanzu Community Edition had a built in `Package Manager` that help with installing, configuring and updating additional application on top of the Kubernetes Cluster it deploys.

For e.g, today Tanzu Community Edition can automatically install Cert-Manager, Knative, Prometheus, Grafana etc. 

A package deployed using Tanzu Community Edition creates equivalent objects in the Kubernetes cluster like, `Deployments`, `Services`, `Persistent Volumes` etc. when applicable.
