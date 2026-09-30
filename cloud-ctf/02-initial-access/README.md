# Step 1: Reconnaissance

## Objective
Identify cluster details and potential attack vectors.

## Commands Used
\`\`\`bash
kubectl cluster-info
kubectl get nodes
kubectl get pods --all-namespaces
kubectl auth can-i --list
\`\`\`

## Findings
- Cluster version: X.XX
- Service accounts with elevated permissions: ...
- Misconfigured RBAC: ...

## Screenshots
![kubectl auth can-i](./screenshots/auth-cani.png)
*Figure 1: RBAC enumeration showing over-permissive service account*

## Analysis
[Explain what you observed and why it matters]

## Next Step
→ [02-initial-access](../02-initial-access/)