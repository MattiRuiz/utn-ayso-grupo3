# UTN - Arquitectura y Sistemas Operativos
Welcome to our repository!

We are Kevin, Matías, Sofía and Facundo, and we are studying Programming at UTN in Rosario.

This is a practical activity to apply knowledge we've learned during the assignment Architecture and Operative Systems.
You can create a cluster, operate it and modify it. Sounds great, right?

If you want to know how it works, here's a step-by-step guide for you to follow:

FRIENDLY REMINDER: to use the commands or web address, ignore the "" at the beggining and the end of the command/web address.

- Download the file called "deploy.yaml" from this repository
- In a Linux's Shell get started Minikube with this command: "minikube start"
- Create the cluster called "grupo3" with this command: "kubectl create namespace grupo3"
- To make sure you did it right type this command: "kubectl get namespaces" that will show a list of namespaces. If you did it right you'd be able to see the namespace called grupo3 on that list.
- To start working on our cluster, one last command: "kubectl config set-context --current --namespace=grupo3

Now we can start working in our cluster. You're doing great!

- Find the path where you've downloaded the file "deploy.yaml"
- Once there, execute this command: "kubectl apply -f deploy.yaml"

Now, all the necessary components will download and then execute. Wait patiently please.

- To know the status of the deployment, try these commands:

"kubectl get deployments" will show the deploy that's executing.
"kubectl get rs" shows the same, including the replica set.
"kubectl get po" show the 3 pods created with the deployment.

To ensure that the Apache server is running properly with its new file "index.html", we have to make sure that it's running in an accesible port, so we have to type another command:

"kubectl port-forward <pod's name> 8080" where in <pod's name> you will paste up one of the names of the pods that you saw when typed "kubectl get po" and the assigned port will be 8080

Now it's time to test it! Let's go!

- Open your navigator and type the following address: "127.0.0.1:8080" or "localhost:8080"

CONGRATULATIONS! You've followed the guide and now you have the entire deployment running properly.
