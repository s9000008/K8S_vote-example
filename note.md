### Kubernetes vote application example

1. 相關服務應用與法
    ```bash
    kubectl apply -f https://raw.githubusercontent.com/dockersamples/example-voting-app/main/k8s-specifications/db-deployment.yaml
    kubectl apply -f https://raw.githubusercontent.com/dockersamples/example-voting-app/main/k8s-specifications/db-service.yaml
    kubectl apply -f https://raw.githubusercontent.com/dockersamples/example-voting-app/main/k8s-specifications/redis-deployment.yaml
    kubectl apply -f https://raw.githubusercontent.com/dockersamples/example-voting-app/main/k8s-specifications/redis-service.yaml
    kubectl apply -f https://raw.githubusercontent.com/dockersamples/example-voting-app/main/k8s-specifications/result-deployment.yaml
    kubectl apply -f https://raw.githubusercontent.com/dockersamples/example-voting-app/main/k8s-specifications/result-service.yaml
    kubectl apply -f https://raw.githubusercontent.com/dockersamples/example-voting-app/main/k8s-specifications/vote-deployment.yaml
    kubectl apply -f https://raw.githubusercontent.com/dockersamples/example-voting-app/main/k8s-specifications/vote-service.yaml
    kubectl apply -f https://raw.githubusercontent.com/dockersamples/example-voting-app/main/k8s-specifications/worker-deployment.yaml
    ```
2. 確認服務病進行投票 
   ```bash
   kubectl describe service vote
   ```
   確認port資訊後進行訪問與投票
3. 訪問投票結果畫面
   ```bash
   kubectl describe service result
   ```
   同步驟2



### 參考資料
- https://birthday.play-with-docker.com/kubernetes-docker-desktop/
- https://github.com/dockersamples/example-voting-app/tree/main
