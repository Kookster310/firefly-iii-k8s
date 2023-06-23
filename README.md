# firefly-iii-k8s
Kubernetes deployment of Firefly III Personal Finance Application

Create namespace: firefly-iii-ns

Create secrets:
  firefly-iii-env: STATIC_CRON_TOKEN=token(32 char long)
  db-env
  
Update cronjob.yaml with token
