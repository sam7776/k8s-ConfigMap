config2-pod.yml > file related commands

# create configmap from a literal value
kubectl create configmap conf-1 --from-literal=food=samosa --from-literal=drink=beer

# get configmap
kubectl get configmap 
/ 
kubectl get cm 

# describe configmap conf-2
kubectl describe cm conf-2

# create pod from file
nano pod-2.yml
kubectl create -f pod-2.yml

# print environment variables of pod-1
kubectl exec pod-2 -- env 
/ 
kubectl exec -it pod-2 -- printenv 