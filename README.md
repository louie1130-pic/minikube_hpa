# minikube_hpa
minikube_hpa

## 步驟
### 建立專案namespace
kubectl create namespace hpa   
### 建立yaml檔
ADD php-apache.yml

### 布署php-apache應用
#### 執行指令
kubectl apply -f .\php-apache.yaml
#### 確認
kubectl get deploy php-apache -n hpa 
'''
NAME         READY   UP-TO-DATE   AVAILABLE   AGE
php-apache   1/1     1            1           73s
'''

### 布署hpa()