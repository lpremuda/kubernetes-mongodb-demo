
Create Secret first, so Deployment can reference it
kubectl apply -f mongo-secret.yaml
kubectl get secret

Create Deployment for MongoDB
kubectl apply -f mongo.yaml

Now that Service has been added to mongo.yaml, redeploy same file
kubectl apply -f mongo.yaml

Create ConfigMap first, so Deployment can reference it
kubectl apply -f mongo-configmap.yaml

Create Deployment for mongo-express
kubectl apply -f mongo-express.yaml

Now that Service has been added to mongo.yaml, redeploy same file
kubectl apply -f mongo-express.yaml

Creates EXTERNAL-IP for mongo-express-service external service
minikube service mongo-express-service