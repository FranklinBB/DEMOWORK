apiVersion: apps/v1
kind: Deployment
metadata:
  name: "frontend-deployment"
  namespace: "2048-game"
spec:
  selector:
    matchLabels:
      app: "frontend"
  replicas: 1
  template:
    metadata:
      labels:
        app: "frontend"
    spec:
      containers:
      - image: nginx
        imagePullPolicy: Always
        name: "frontend"
        ports:
        - containerPort: 80

