```bash
> kubectl get po,sts,svc,pvc
NAME             READY   STATUS    RESTARTS   AGE
pod/devops-workflow-0                         1/1     Running            0                  25s
pod/devops-workflow-1                         1/1     Running            0                  25s
pod/devops-workflow-2                         1/1     Running            0                  25s

NAME                               READY   AGE
statefulset.apps/devops-workflow   3/3     25s

NAME                             TYPE           CLUSTER-IP     EXTERNAL-IP   PORT(S)          AGE
service/devops-devops-workflow   LoadBalancer   10.109.59.6    <pending>     5000:30396/TCP   7d17h
service/devops-workflow          LoadBalancer   10.102.86.67   <pending>     8000:31791/TCP   25s
service/kubernetes               ClusterIP      10.96.0.1      <none>        443/TCP          14d

NAME                                             STATUS   VOLUME                                     CAPACITY   ACCESS MODES   STORAGECLASS   AGE
persistentvolumeclaim/visits-devops-workflow-0   Bound    pvc-1a04dc10-cca6-4436-9cd7-efb29db36152   256M       RWO            standard       21m
persistentvolumeclaim/visits-devops-workflow-1   Bound    pvc-883ec4db-05e1-446a-9567-1ded48366461   256M       RWO            standard       21m
persistentvolumeclaim/visits-devops-workflow-2   Bound    pvc-235747dc-212f-4522-aa1f-2901db888f59   256M       RWO            standard       21m
```
