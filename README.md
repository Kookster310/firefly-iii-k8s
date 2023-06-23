# firefly-iii-k8s
#Kubernetes deployment of Firefly III Personal Finance Application

###Create namespace: firefly-iii-ns

###secrets.yaml file to configure application

###Required updates:

| Location | Parameter | Example Value | Notes |
| ------ | ------ | ------ | ------ |
| secrets.yaml/firefly-iii-env | APP_KEY  | 57g43itrdz8orzw57mfky3tn3d5x3wri | 32 character long string |
| secrets.yaml/firefly-iii-env | DB_PASSWORD | kd4XUMPFebcehrBjLkKH | mysql password for firefly user |
| secrets.yaml/firefly-iii-env | MAIL_PASSWORD | 9NLMpuKWM7BCvbfcGPB5 | SMTP password |
| secrets.yaml/firefly-iii-env | STATIC_CRON_TOKEN | X5e7caQUuGQBRtjn9UoqZx3SnaUJj39g | must be *exactly* 32 characters long |
| secrets.yaml/db-env | MYSQL_PASSWORD | kd4XUMPFebcehrBjLkKH | mysql paassword for firefly user, must match DB_PASSWORD |
| secrets.yaml/importer-env | MAIL_PASSWORD | 9NLMpuKWM7BCvbfcGPB5 | SMTP password |
| cronjob.yaml | command | X5e7caQUuGQBRtjn9UoqZx3SnaUJj39g | update the REPLACEME string with the token created for STATIC_CRON_TOKEN |
