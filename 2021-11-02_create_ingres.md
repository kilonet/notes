
```
kilonet@kilonet-MacBookPro:~/dev/dictionary-service$ kubectl expose deployment eis-dictionary-service-deployment -n orion-test --type=NodePort
service/eis-dictionary-service-deployment exposed
kilonet@kilonet-MacBookPro:~/dev/dictionary-service$ minikube service eis-dictionary-service-svc -n orion-test
|------------|----------------------------|-------------|--------------|
| NAMESPACE  |            NAME            | TARGET PORT |     URL      |
|------------|----------------------------|-------------|--------------|
| orion-test | eis-dictionary-service-svc |             | No node port |
|------------|----------------------------|-------------|--------------|
😿  service orion-test/eis-dictionary-service-svc has no node port
kilonet@kilonet-MacBookPro:~/dev/dictionary-service$ minikube service eis-dictionary-service-deployment -n orion-test
|------------|-----------------------------------|-------------|---------------------------|
| NAMESPACE  |               NAME                | TARGET PORT |            URL            |
|------------|-----------------------------------|-------------|---------------------------|
| orion-test | eis-dictionary-service-deployment |        9993 | http://192.168.49.2:30101 |
|------------|-----------------------------------|-------------|---------------------------|
🎉  Opening service orion-test/eis-dictionary-service-deployment in default browser...
kilonet@kilonet-MacBookPro:~/dev/dictionary-service$ Opening in existing browser session.
```

```
kilonet@kilonet-MacBookPro:~/dev/dictionary-service$ eval $(minikube docker-env)
kilonet@kilonet-MacBookPro:~/dev/dictionary-service$ docker build -t localhost:5000/dictionary-service:test .
```

