# Adjust goguerrilla's config file
kubectl -- create configmap goguerrilla-cf --from-file=goguerrilla.conf.json
# Sanity Check
kubectl get cm goguerrilla-cf -n default -o yaml
