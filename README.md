# fizz-gateway-k8s
Kubenetes deployment yaml demo for fizz-gateway

## 创建 `fizz-gateway` 服务

### 1. 生成 configmap：

```shell
kubectl create configmap -n fizz-gateway fizz-gateway-config --from-file gateway/application.yml 
```

### 2. 创建 service（nodePort）

```shell
kubectl apply -f gateway/service.yml
```

### 3. 创建 deployment

```shell
kubectl apply -f gateway/deployment.yml
```

### 4. 创建ingress

```shell
kubectl apply -f gateway/ingress.yml
```


## 创建 `fizz-manager` 服务

### 1. 生成 configmap：

```shell
kubectl create configmap -n fizz-gateway fizz-manager-config --from-file manager/application.yml 
```

### 2. 创建 service（nodePort）

```shell
kubectl apply -f manager/service.yml
```

### 3. 创建 deployment

```shell
kubectl apply -f manager/deployment.yml
```

### 4. 创建ingress

```shell
kubectl apply -f manager/ingress.yml
```

