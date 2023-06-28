### Deploying a Chart to Kubernetes Cluster

Confirm Helm version
```$ helm version```

Add a helm repository to use the charts in the following demos using this custom repository as the charts in the stable repository have been deprecated.
```$ helm repo add andrewpruski https://raw.githubusercontent.com/dbafromthecold/KubernetesPackageAdminWithHelm/master/```

Search for a chart
```$ helm search repo andrewpruski/mysql```

Confirm current context
```$ kubectl config current-context```

Test connection to cluster
```$ kubectl get nodes```

List helm repositories
```$ helm repo list```

Search repository for a mysql chart
```$ helm search repo andrewpruski/mysql```

Show chart definition
```$ helm show chart andrewpruski/mysql```

Show chart README
```$ helm show readme andrewpruski/mysql```

Pipe README to file
```$ helm show readme andrewpruski/mysql > C:\Temp\README.txt```

Show chart values
```$ helm show values andrewpruski/mysql > C:\Temp\values.txt```

Test deployment of chart
```$ helm install mysql andrewpruski/mysql --dry-run --debug```
Deploy chart
```$ helm install mysql andrewpruski/mysql```

Confirm deployment
```$ helm list```
