# Ejercicio 9

1. Aplicar el deployment

```
kubectl apply -f deployment.yaml
```

2. Obtener el nombre de un pod

```
kubectl get pods
```

3. Ingresar a un pod

```
kubectl exec -it passwordapiapp-666ccf6fbc-rc7bc --  bash
```

4. Dentro del pod, verificar el funcionamiento

```
curl localhost:3000/password 
```