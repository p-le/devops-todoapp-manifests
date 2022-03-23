## Using GitHub Action Workflow  `kustomize`

### Workflow `.github/workflows/deploy.yaml`

This Workflow will need to be triggered manually after merging Pull Requests.

Pull Requests will be created when you build container images in Frontend and Backend Repositories
- https://github.com/p-le/devops-todoapp-backend/blob/main/.github/workflows/build.yaml
- https://github.com/p-le/devops-todoapp-frontend/blob/main/.github/workflows/build.yaml

Steps:

1. Authenticate to GCP Project using Workload Identity Feature
2. Authorize to target GKE Cluster
3. Install Kustomize
4. Apply Kubernetes Manifest Files. Replace value using `sed`


## Migration to Helm Chart
Note: IMO, Kustomize's template feature does not support provide variables dynamically.

That's why I used `sed` command to replace values in Manifest Files as a workaround.

I've decided to use Helm Chart with ArgoCD.

Check Repository: https://github.com/p-le/devops-helm-charts