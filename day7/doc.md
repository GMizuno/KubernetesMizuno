# Comandos para executar

Apos realizar o apply dos dois arquivos yaml, realizar o seguintes comandos


Listar os comando

``` bash
kubectl get service
```

Acessar Pod nginx-0 e criar arquivo index.html com TESTE-0 

```bash
kubectl exec -it nginx-0 -- bash
cd /usr/share/nginx/html
echo "TESTE-0" > index.html
``` 

Acessar Pod nginx-1 e criar arquivo index.html com TESTE-1 

```bash
kubectl exec -it nginx-1 -- bash
cd /usr/share/nginx/html
echo "TESTE-1" > index.html
``` 

Acessar Pod nginx-2 criar arquivo index.html com TESTE-2

```bash
kubectl exec -it nginx-2 -- bash
cd /usr/share/nginx/html
echo "TESTE-2" > index.html
``` 

```bash
kubectl exec -it nginx-1 -- bash
curl nginx-0.nginx.default.svc.cluster.local
``` 

```bash
kubectl exec -it nginx-2 -- bash
curl nginx-0.nginx.default.svc.cluster.local
``` 

```bash
kubectl exec -it nginx-2 -- bash
curl nginx-0.nginx.default.svc.cluster.local
``` 