To switch between namespace in k8s
alias kubens='kubectl config set-context --current --namespace '
kubens kube-system //Switch to a different namespace
Systemports → In the kubernetes environment non-root users can not use ports from 1 to 1023 in nginx configuration.
Also if we need to change the nginx server listen at 8080 
Also allow ports in aws security group from 30000 to 32767 on K8s nodes for load balancer service.
