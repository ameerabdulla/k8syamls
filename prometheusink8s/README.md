create container of prometheus from prometheus image using deploy file.
apply deployment.yml
create config.yml containing conf of prometheus for help download prometheus from link and unzip and cat prometheus.yml
apply config.yml
create loadbalancer and apply 
create image of node-exporter with dockerfile
push image into dockerhub repo
create nodedeploy.yml file and apply 
then apply Loadbalancer file for node balancer

in config.yml file  of server, add ip of 'node-exporter pod' with public port given by loadbalancer in targets.

hit public ip of instance with port given by loadbalancer for access prom or node-exp. 
