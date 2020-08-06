# iop v3

kubectl apply -f reva-pvc.yaml

helm install iop sciencemesh/iop --set gateway.persistentVolume.enabled=true --set gateway.persistentVolume.existingClaim=iop-pvc --set-file gateway.configFiles.revad\\.toml=standalone.toml --set-file gateway.configFiles.gateway\\.toml=standalone.toml --set-file gateway.configFiles.users\\.json=users-ailleron.json --set-file gateway.configFiles.ocm-providers\\.json=providers.demo.json -f home-sp.yaml -f reva-sp.yaml

# iop v4

kubectl apply -f reva-pvc.yaml 

helm install iop sciencemesh/iop --set gateway.persistentVolume.enabled=true --set gateway.persistentVolume.existingClaim=iop-pvc --set-file gateway.configFiles.revad\\.toml=standalone.toml --set-file gateway.configFiles.gateway\\.toml=standalone.toml --set-file gateway.configFiles.users\\.json=users-ailleron.json -f home-sp.yaml -f reva-sp.yaml
