# Step 1: Reconnaissance

## Objective
Enumerate the EKS cluster to identify:
- Cluster version, nodes, and namespaces
- RBAC permissions of the current identity
- Running workloads and exposed services
- Potential misconfigurations and attack vectors

## Environment
- **Cluster:** AWS EKS
- **Access method:** [e.g., provided kubeconfig / assumed IAM role / SSRF to IMDS]
- **Tools used:** `kubectl`, `aws-cli`, `kubelet`, `trivy` (optional)

---

## 1.1 Identify Current Context & Identity

First, confirm which cluster and identity we're operating as.

```bash
kubectl config current-context
kubectl config view --minify
kubectl cluster-info