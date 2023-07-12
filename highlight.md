# Highlight tests

```yaml linenos
capacity.yaml
apiVersion: req.nephio.org/v1alpha1
kind: Capacity
metadata: # kpt-merge: /control-plane
  name: control-plane
  annotations:
    config.kubernetes.io/local-config: "true"
```
```yaml {highlight=1}
    specializer.nephio.org/owner: workload.nephio.org/v1alpha1.SMFDeployment.smf-regional
```
```yaml
    specializer.nephio.org/namespace: free5gc-cp
    internal.kpt.dev/upstream-identifier: 'req.nephio.org|Capacity|default|control-plane'
spec:
  maxSessions: 500
  maxNFConnections: 5
```


