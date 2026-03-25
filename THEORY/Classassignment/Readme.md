# 🚀 Hello Web App using Kubernetes (Apache httpd)

## 🎯 Objective
Deploy and manage a simple Apache web server using Kubernetes.  
Verify it is running, modify it, scale it, and debug it.

---

  **Step 1: Create Deployment**
  ```bash

  kubectl create deployment hello-web --image=httpd
  
  ```
  ![deployment](1.png)
  
  **Step 2: Verify Deployment**
  ```bash
  kubectl get deployments
  ```
  ![deployments](2.png)

**Step 3: Verify pods**
  ```bash
  kubectl get pods
  ```
  ![pods](3.png)

  **Step 4: Expose deployment**
  ```bash
  kubectl expose deployment hello-web --type=NodePort --port=80
  ```
  ![expose](4.png)

  **Step 5: Verify Service**
  ```bash
  kubectl get services
  ```
  ![service](5.png)

   **Step 6: Create HTML File**
  ```bash
  notepad index.html
  ```
  ![html](6.png)

  ![file](7.png)

 **Step 7: Create ConfigMap**
  ```bash
  kubectl create configmap my-html --from-file=index.html
  ```
  ![config](8.png)
  
   **Step 8: Verify ConfigMap**
  ```bash
  kubectl describe configmap my-html
  ```
  ![config1](9.png)
  **Step 9: Edit Deployment**
  ```bash
  kubectl edit deployment hello-web
  ```
  ![edit](10.png)
  ![edit1](11.png)
**Step 10: Restart Deployment**
  ```bash

  kubectl rollout restart deployment hello-web

  ```

  ![restart](12.png)
  **Step 11: Verify Pods Again**
  ```bash
  kubectl get pods
  ```
  ![new pods](13.png)
  **Step 12: Verify File inside Pod**
  ```bash
  kubectl exec -it <pod-name> -- cat /usr/local/apache2/htdocs/index.html
  ```
  ![verify](14.png)
  **Step 13: Access Application**
  ```bash
  kubectl port-forward pod/hello-web-c7495c66-n5fzw 8081:80
  ```
  ![port](15.png)
  ![url](16.png)
  **Step 14: Scale Deployment**
  ```bash
  kubectl scale deployment hello-web --replicas=3
  ```
  ![port](17.png)
  **Step 15: Verify Scaling**
  ```bash
 kubectl get pods
  ```
  ![port](18.png)
  **Step 16: Check Logs**
  ```bash
 kubectl logs  hello-web-c7495c66-n5fzw
  ```
  ![port](19.png)









  
