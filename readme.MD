To switch between namespace in k8s
alias kubens='kubectl config set-context --current --namespace '
kubens kube-system //Switch to a different namespace
Systemports → In the kubernetes environment non-root users can not use ports from 1 to 1023 in nginx configuration.
Also if we need to change the nginx server listen at 8080 
Also allow ports in aws security group from 30000 to 32767 on K8s nodes for load balancer service.



EBS for Mysql
1. assign ebscsidrivepolicy role to one of the nodes 
2. ebs volume should be nodes AZ
3. install EBS volume drivers on cluster = kubectl apply -k "github.com/kubernetes-sigs/aws-ebs-csi-driver/deploy/kubernetes/overlays/stable/?ref=release-1.39"
4. Storage class created by admins
5. While crerating PVC we give Storage class
6. When kubectl apply pvc it automatically/dynamically creates PV and external volume AWS EBS