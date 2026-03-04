OpenID Connect Create
```
eksctl utils associate-iam-oidc-provider --cluster roboshop-dev --approve
```
```
eksctl create iamserviceaccount --cluster <cluster-name> --name <service-account-name> --namespace <namespace> --attach-policy-arn <IAM-policy-ARN> -- approve
```

eksctl create iamserviceaccount --cluster roboshop-dev --name secret-reader --namespace roboshop --attach-policy-arn arn:aws:iam::167819473967:policy/RoboShopMySQLSecretReader --approve 

aws secretmanager get-secret-value --secret-id roboshop/dev/mysql_password --query SecretString --output text