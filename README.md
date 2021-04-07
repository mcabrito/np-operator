# Operator Network Policy

```yaml
apiVersion: np-operator-policies.bells17.io/v1alpha1
kind: OperadorNetworkPolicy
metadata:
  labels:
    controller-tools.k8s.io: "1.0"
  name: sample-networkpolicy
spec:
  namePrefix: common
  excludeNamespaces:
  - kube-system
  - common-network-policy-operator-system
  policySpec:
    podSelector: {}
    policyTypes:
    - Egress

---
apiVersion: np-operator-policies.bells17.io/v1alpha1
kind: OperadorNetworkPolicy
metadata:
  labels:
    controller-tools.k8s.io: "1.0"
  name: sample-networkpolicy2
spec:
  namePrefix: common
  excludeNamespaces:
  - kube-system
  - common-network-policy-operator-system
  policySpec:
    podSelector: {}
    ingress:
    - {}
```
