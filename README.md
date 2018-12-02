
submit and create a deployment for k8s 

  
    :param task_info: a dict representing the detail of a task, e.g.
       {
           name: "redis"
           namespace: "default"
           image: "redis",   # required
           replicas: 3
           resource: {
               cpu: 2000m,
               gpu: 2000m,
               mem: 2Gi
           }
       },
    :command
        submit --namespace=default --resource='{"cpu":"100m", "memory":"1Gi"}'  --name=redis --image=redis --replicas=3


delete a deployment for k8s

    :param name: deploy_name
    {
        namespace: "default"
        name: "redis"
    },
    :command
        delete --name=redis --namespace=default
        
get deployments info

    :param namespace: deploy_name
    {
        namespace: "default" (not required, None for all namespace)
    },
    :command
        get_deployments --namespace=default
        get_deployments

get one deployment info

    :param namespace: deploy_name
    {
        name: "redis"
        namespace: "default" 
    },
    :command
        get_deployment --namespace=default --name=redis
     

update a deployment for k8s 

  
    :param task_info: a dict representing the detail of a task, e.g.
       {
           name: "redis"
           namespace: "default"
           image: "redis",   # required
           replicas: 3
           resource: {
               cpu: 2000m,
               gpu: 2000m,
               mem: 2Gi
           }
       },
    :command
        update_deployment --namespace=default --resource='{"cpu":"100m", "memory":"1Gi"}'  --name=redis --image=redis --replicas=2

get k8s node info

    :param : no args needed
           
    :command
        list_node
           