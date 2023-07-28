# firefly-iii-k8s
#Kubernetes deployment of Firefly III Personal Finance Application


###See: https://github.com/firefly-iii/kubernetes/tree/main/charts
tldr: 
```helm repo add firefly-iii https://firefly-iii.github.io/kubernetes
helm repo update
helm install firefly-iii firefly-iii/firefly-iii-stack```


###Suggested values.yaml on helm install:
```
firefly-db:
  storage:
    class: local-path
    dataSize: 10Gi
  configs:
    TZ: Pacific/Honolulu
  backup:
    pvc:
      class: local-path
      dataSize: 10Gi

firefly-iii:
  persistence:
    storageClassName: local-path
    storage: 10Gi
  cronjob:
    enabled: true
    auth:
      token: X5e7caQUuGQBRtjn9UoqZx3SnaUJj39g

importer:
  fireflyiii:
    url: "https://firefly.310networks.com"
    auth:
      accessToken: X5e7caQUuGQBRtjn9UoqZx3SnaUJj39g
  config:
    env:
      TZ: Pacific/Honolulu