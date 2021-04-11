# CreatingPod
## Create a pod of docker.io/openshift/hello-openshift and try to access using curl 

### On master Node

`$ kubectl apply -f "https://cloud.weave.works/k8s/net?k8s-version=$(kubectl version | base64 | tr -d '\n')" `

`$ kubectl get pods -n kube-system`

`$ kubectl get nodes`


`$ vi mypod1.yml`
<p>apiVersion: v1<br>
kind: Pod<br>
metadata:<br>
  name: apache3<br>
  labels:<br>
    mycka: simplilearn<br>
spec:<br>
  containers:<br>
  - name: mycontainer<br>
    image: docker.io/openshift/hello-openshift<br>
    ports:<br>
    - containerPort: 80</p>

`$ kubectl create -f mypod1.yml`<br>
`$ kubectl get pods`<br>
`$ kubectl get pods -owide`<br>
`$ kubectl get pods -o wide`<br>
`$ curl 10.44.0.1:8080`<br>


