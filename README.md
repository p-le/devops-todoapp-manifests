## Using `kustomize`

### 1. Update Images

```
kustomize edit set image "todoapp-frontend=asia-northeast1-docker.pkg.dev/phu-le-it/todoapp-repository/todoapp-frontend:1.0.4"
```

```
kustomize edit set image "todoapp-backend=asia-northeast1-docker.pkg.dev/phu-le-it/todoapp-repository/todoapp-backend:1.0.9"
```