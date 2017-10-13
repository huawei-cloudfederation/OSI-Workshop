Create Deployment :
 Use the deployment.yaml  file to create the deployment
kubectl create –f deployment.yaml
 List the deployments:
	Kubectl get deployment
List the replicaset
               Kubectl get rs
List the pods
              Kubectl get pods
  Details of the pod
Kubectl describe pods
Getting inside the container 
kubectl exec –it [podname]  -- /bin/bash
Delete the pod 
	Kubectl delete pod [podname]
Scale the replicas : 
kubectl scale deployment [deployment name] --replicas=10
Install heapster :
kubectl apply -f  https://raw.githubusercontent.com/kubernetes/kops/master/addons/monitoring-standalone/v1.6.0.yaml
install cadvisor:
sudo apt-get install cadvisor
create the deployment using autoscaledeployment.yaml
       kubectl create –f autoscaledeployment.yaml
Autoscale the deployment :
kubectl autoscale deployment  autoscaledeployment --cpu-percent=10 --min=1 --max=10
Exec into the pod and run the load
for i in 1 2 3 4; do while : ; do : ; done & done
watch kubectl get hpa to see the increase in the cpu utilization.
 Replicas of the pod increase when the load increases.
Delete the pod which is stressed the replica count will come down.

PDB: 
Create a poddisruptionbudgets with maxUnavailable as 1
Kubectl create –f pdb.yaml
Drain one of slave node:
 kubectl drain raj-slave2 --ignore-daemonsets
watch the deployment  and pod to see how they are deleted.

Affinity :
Create the deployment redis-cache 
          Kubectl create –f redisaffinity.yaml
Create the deployment web-server
       Kubectl create –f webaffinity.yaml
Check which nodes the pods are scheduled
Both of the pods are in the same node.
