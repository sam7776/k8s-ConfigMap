**config3-pod.yml > file related commands**

# create file with any name and extension like my-file.txt and store data
nano my-file.txt

# create configmap from file
kubectl create configmap conf-3 --from-file=my-file.txt 

# get configmap
kubectl get configmap 
/
kubectl get cm 

# describe configmap conf-3
kubectl describe cm conf-3

# to get data from configmap in pod-3
kubectl exec pod-3 -- ls /etc/config 
/
kubectl exec pod-3 -- cat /etc/config/my-file.txt
/
# to get the shell of the pod
# after entering go to the path > where my-file.txt (FILE) are located
kubctl exec -it pod-3 -- /bin/bash 
*>>>/ cd /etc/config
*>>>/ ls 
*>>>/ cat my-file.txt