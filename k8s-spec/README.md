### To create configmaps

Ref. to file - cm-1.yaml

Firstly, prepare a configmap which carries your username and password as a service

```
kubectl create configmap configmap-1 --from-literal=username=tauqeerahmad5201 --from-literal=password=##4f53fgh
```

cm-1.yaml has some cofiguration to consider the configmap as an object as a whole. 

```
kubectl apply -f cm-1.yaml
```



Ref. to file - cm-2.yaml

```
kubectl create configmap configmap-2 --from-literal=name
```
cm-2.yaml has some configuration to directly point towards the key value rather than holding whole yaml file as an object. 



Ref. to file - cm-3.yaml

```
kubectl create configmap configmap-3 --from-file=data-file
```
In this case, we have data-file which carries your env data or config. 

