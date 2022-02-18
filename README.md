# TODO

## Update `backend.yaml`
1. Change email of Node Pool Account
```
metadata:
  annotations:
    iam.gke.io/gcp-service-account:
```

2. Change target of Container Image:
```
spec:
  template:
    spec:
      containers:
        - name: todoapp-backend
          image:
```
3. Change Cloud SQL Database Connection Name:
```
spec:
  template:
    spec:
      containers:
        - name: cloudsql-proxy
          command:
            - instances=
```


## Update `frontend.yaml`

2. Change target of Container Image:
```
spec:
  template:
    spec:
      containers:
        - name: todoapp-frontend
          image: