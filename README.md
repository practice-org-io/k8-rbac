# Kubernetes RBAC

Role-Based Access Control exercises for Kubernetes. 8 YAML files covering roles, role bindings, service accounts, and AWS IAM integration.

## Files

| File | Purpose |
|---|---|
| `01-role.yaml` | ClusterRole definition |
| `02-role-binding.yaml` | Binds role to a user |
| `03-aws-auth.yaml` | AWS IAM role mapping |
| `04-roboshop-admin.yaml` | Admin ClusterRole |
| `05-roboshop-admin-rb.yaml` | Admin ClusterRoleBinding |
| `06-trainee-role-binding.yaml` | Trainee role binding |
| `07-sa.yaml` | ServiceAccount definition |
| `08-pod.yaml` | Pod using a ServiceAccount |

## Key Patterns

- **ClusterRole vs Role** — Cluster-wide vs namespace-scoped permissions
- **RoleBinding vs ClusterRoleBinding** — Who gets what access
- **ServiceAccounts** — Identity for pods and processes
- **AWS IAM mapping** — `aws-auth.yaml` maps IAM roles to K8s users

## Quick Start

```bash
kubectl apply -f .
kubectl auth can-i --as trainee create pods
```

## Related Practice
