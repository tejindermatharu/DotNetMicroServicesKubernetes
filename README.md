https://github.com/dotnet-architecture/eShopOnContainers/tree/dev/deploy/k8s

# .NET Microservices Kubernetes Sample Application

## Getting Started

Make sure you have installed docker desktop on your machine. If windows, then make sure you have window sub system for linux installed too.

You could either run the application with docker compose using visual studio.

Or you can still run with container support using IIS Express by using the multiple start up projects options as below:

![image](https://user-images.githubusercontent.com/17796549/114305777-7cf1dd00-9ad1-11eb-86ae-5800a80a20cc.png)

After that to run these containers using a local kubernetes cluster (ensure you have kubernetes enabled via Docker Desktop) , you can run the below command from the rootdirectory.

```powershell
docker-compose build
```

Then run docker images and make sure that you see two images:

weatherweb: latest
weatherapi: latest

Then you can run from root directory:

```powershell
kubectl apply -f deployment.yml 
```

Run:

```powershell
kubectl get all
```

You should see two pods running in the pods section:

![image](https://user-images.githubusercontent.com/17796549/114306149-d8709a80-9ad2-11eb-9a4a-5a541b28279e.png)

Then browse to http://localhost

![image](https://user-images.githubusercontent.com/17796549/114306178-f63dff80-9ad2-11eb-9009-fc7f67985763.png)



