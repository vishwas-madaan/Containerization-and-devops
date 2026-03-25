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
  

  
