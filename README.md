### Front end
- yarn build
- docker build -t xaelkaz/frontend:1 .  
### API
- CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -o api
### K8s
- kubectl apply -f namespace.yaml
- kubectl config set-context --current --namespace=cloudacademy
- watch kubctl get all,pv,pvc