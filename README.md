## Kubernetes Setup and Deployment Guide

### Enable Kubernetes

1. **Verify Kubernetes Cluster Info**:
    ```bash
    kubectl cluster-info
    kubectl get nodes
    ```
    ![Cluster Info](https://github.com/gaurav3444/sit323-737-2024-t1--prac7p/assets/66586901/8aa60a28-e84d-486e-8dc2-dcb8e4f516bb)


### Build and Push Docker Image

1. **Build Docker Image**:
    ```bash
    docker build -t yourusername/yourimage:latest .
    ```
    ![Docker Build](https://github.com/gaurav3444/sit323-737-2024-t1--prac7p/assets/66586901/8718a482-8f9a-4f04-8ce1-dadfc80a18b8)


2. **Tag and Push Image**:
    ```bash
    docker push yourusername/yourimage:latest
    ```
    ![Docker images](https://github.com/gaurav3444/sit323-737-2024-t1--prac7p/assets/66586901/324fc272-189c-4d01-b2d1-f27ddb3c2062)
    ![Docker tag](https://github.com/gaurav3444/sit323-737-2024-t1--prac7p/assets/66586901/68971201-2a38-46e5-afe1-1c21b170bb0d)
    ![Docker Push](https://github.com/gaurav3444/sit323-737-2024-t1--prac7p/assets/66586901/5c4fd9c1-86e7-4f9c-8275-db84158fcaab)


### Create Kubernetes Deployment and Service

1. **Create Pods**:
    ```bash
    kubectl apply -f ./createPods.yaml
    ```
    ![Create Pods](https://github.com/gaurav3444/sit323-737-2024-t1--prac7p/assets/66586901/a2e43063-9dbd-4795-919f-c3e7bb80c394)


2. **Create Replica Set**:
   Replica Sets ensure that a specified number of pod replicas are running at any given time. They are useful for ensuring high availability of your application.
   To create a Replica Set, use the following command:
    ```bash
    kubectl apply -f ./createReplicaSet.yaml
    ```
    ![Create Replica Set](https://github.com/gaurav3444/sit323-737-2024-t1--prac7p/assets/66586901/fd263aac-abf0-49ee-b340-13ac4622c730)


4. **Create Deployment**:
    ```bash
    kubectl apply -f ./createDeployment.yaml
    ```
    ![Create Deployment](https://github.com/gaurav3444/sit323-737-2024-t1--prac7p/assets/66586901/d2afba9e-e1da-4c3e-8b40-c5fc09e503ad)
 

5. **Create Service**:
    ```bash
    kubectl apply -f ./createService.yaml
    ```
    ![Create Service](https://github.com/gaurav3444/sit323-737-2024-t1--prac7p/assets/66586901/8fdfef71-5469-4d76-8a5b-1e55d7f9dd6c)

6. **Verify Service**:
    After applying the Service configuration, use `kubectl get svc` to verify the status of the service, including its ClusterIP or NodePort.
    ![Verify Service](https://github.com/gaurav3444/sit323-737-2024-t1--prac7p/assets/66586901/e17ef0db-9f43-47d6-8471-d338661f66b9)
