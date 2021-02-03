# Clair en K8s

- Files
    - **config.yaml** ( Archivo de configuraciones de Clair, se puede aplicar como secreto )
    - **clair-k8s.yaml** ( Manifiestos de Clair con el secret )

## Procedimiento
He dejado dos formas de despliegue, un all in one para aplicar solo un archivo o de forma separada. 

- All in one
```bash
kubectl apply -f ./k8s/all-in-one-clair.yaml
```

- Primero el secret y luego los manifiestos
```bash
kubectl create secret generic clairsecret --from-file=./k8s/config.yaml
kubectl apply -f ./k8s/clair-k8s.yaml
```

### Todo
- VPC


Ref:
- https://coreos.com/clair/docs/latest/
- 
