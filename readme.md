# Before the demo, verify steps 1 and 2

- 1 - Set the cluster up

- 2 - Verify if voting-k8s dir is in the environment. If not, do: git clone https://github.com/kaiohenricunha/k8s-voting-app

- 3 - Explain K8s high-level architecture

- 4 - Explain Kubeconfig

- 5 - Explain Namespaces

- 6 - Explain Resource Quota

- 7 - Create a Namespace called 'playground': kubectl create namespace playground. If necessary, command to switch Namespace: kubectl config set-context $(kubectl config current-context) --namespace=playground / kubens playground

- 8 - Give one more example on how to access different services on different namespaces.

- 9 - Explain Pods

- 10 - Explain Deployments

- 11 - Explain StatefulSets

- 12 - Show StatefulSets in practice

- 13 - Explain Jobs

- 14 - Demonstrate Jobs:
    - kubectl create -f throw-dice-job.yaml -n playground
    - kubectl get jobs -n playground
    - kubectl get pods -n playground
    - kubectl logs nome-do-pod -n playground
    - How many attempts: kubectl describe job throw-dice-job -n playground
    - kubectl delete job throw-dice-job -n playground

- 15 - Explain Cronjobs

- 16 - Demonstrate Cronjobs: 
    - kubectl create -f throw-dice-cron-job.yaml -n playground
    - kubectl get cronjob -n playground
    - kubectl describe cronjob throw-dice-cron-job -n playground
    - kubectl delete cronjob throw-dice-cron-job -n playground

- 17 - Explain Services

- 18 - Show my own Service files. Demonstration in the end.

- 19 - Show my redis svc and voting svc to exemplify ClusterIPs

- 20 - Explain Ingress

- 21 - Ingress Practice: 
    - minikube addons enable ingress
    - to verify nginx: kubectl get services --all-namespaces
    - kubectl get all

- 22 - Explain ConfigMaps

- 23 - ConfigMap Practice:
    - move to the right dir and apply

- 26 - Explain Secrets

- 27 - Secrets in Practice

- 28 - Explain Volumes

- 29 - Show Volumes in Practice

- 30 - Explain PVC

- 31 - Show PVC in Practice

- 32 - Explain Custom Resources

- 33 - Show Custom Resources in Practice

- 34 - Demonstrate my application:
    - move to ingress-playground folder and apply everything(remmember to set the ClusterIP on nano. The voting-k8s folder app doesn't use Ingress)
    - then, demonstrate the application's interface