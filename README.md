# Project Name: Kubernetes Nginx Pods Example

## Overview
This project demonstrates the process of managing Kubernetes resources, including namespaces and pods. The `kubekart` namespace was created, and two Nginx pods were deployed in it.

## Steps
1. **Start Minikube**: 
   - Use `minikube start` to initiate a local Kubernetes cluster.
   - Kubernetes components are verified, and addons are enabled.
   
2. **Create a Namespace**: 
   - A new namespace `kubekart` was created using the command:
     ```bash
     kubectl create ns kubekart
     ```

3. **Deploy Pods**: 
   - Two Nginx pods (`nginx1` and `nginx12`) were deployed within the `kubekart` namespace using:
     ```bash
     kubectl run nginx1 --image=nginx -n kubekart
     kubectl apply -f pod.yaml
     ```

4. **Verify Pods**: 
   - Pods were verified using:
     ```bash
     kubectl get pod -n kubekart
     ```

5. **Delete Namespace**:
   - The namespace `kubekart` was successfully deleted with:
     ```bash
     kubectl delete ns kubekart
     ```

## Requirements
- Minikube
- Kubernetes CLI (kubectl)


## Clone the Repository

To clone this repository to your local machine, run the following command:

```bash
git clone https://github.com/AditiPandey568/namespace-kubernates.git

## Future Work
- Expand the setup to include more complex services like LoadBalancers or StatefulSets.
- Explore Helm charts for easier management of Kubernetes applications.

## Contact
For questions, feel free to reach out to Aditi Pandey at pandeyaditi0307@gmail.com.
