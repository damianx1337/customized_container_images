# Adjust postfix master.cf (get it from /etc/postfix directory or use this one)
kubectl -- create configmap postfix-master-cf --from-file=master.cf
# Sanity Check
kubectl get cm postfix-master-cf -n default -o yaml
