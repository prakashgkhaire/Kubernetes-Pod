`kubectl create deployment test2 --image=docker.io/openshift/hello-openshift`<br>
`kubectl scale deployment test2 --replicas=2`<br>
`kubectl get pods`<br>
`kubectl get pods  -o wide`<br>
`kubectl get pods  --show-labels`<br>
`kubectl expose deployment test2 --port=80`<br>
`kubectl get svc`<br>
`kubectl describe svc test2`<br>
`kubectl scale deployment test2 --replicas=3`<br>
`kubectl describe svc test2`<br>
