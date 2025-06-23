config1-pod.yml > file related commands

# create configmap from a literal value 
kubectl create configmap conf-1 --from-literal=name=AnthonyGonsalwis

# get configmap
kubectl get configmap 
/ 
kubectl get cm 

# describe configmap conf-1
kubectl describe cm conf-1 

# create pod from file
nano pod-1.yml
kubectl create -f pod-1.yml 

# print environment variables of pod-1
kubectl exec pod-1 -- env 
/ 
kubectl exec -it pod-1 -- printenv 
