# mysql-db-openshift
tech tejendra:

oc new-app --as-deployment-config --docker-image=registry.access.redhat.com/rhscl/mysql-57-rhel7:latest --name=mysql-openshift -e MYSQL_USER=user1 -e MYSQL_PASSWORD=mypa55 -e MYSQL_DATABASE=testdb -e MYSQL_ROOT_PASSWORD=r00tpa55
oc status
oc get pods
oc describe pod {pod-id}
oc get svc
oc describe service mysql-openshift
oc describe dc mysql-openshift
oc expose service mysql-openshift
oc get routes
oc port-forward {pod-id} 3306:3306
oc port-forward mysql-openshift-1-gbz8d 3306:3306


mysql --password=mypa55 --user=user1

from template:

oc create -f mysql-template.yaml
mysql --password=r00tpa55 --user=root


