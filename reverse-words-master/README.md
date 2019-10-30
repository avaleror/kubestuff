**Get reverse word**

```sh
curl http://127.0.0.1:8080/ -X POST -d '{"word":"PALC"}'
{"reverse_word":"CLAP"}
```
If you´re planning to test the app from the outside of the cluster you need to create a route inside the OpenShift or Kubernetes Cluster. Then you´ll have to query the endpoint created for the app.

```sh
curl -k reverse-default.apps.cluster-1234.example.com -X POST -d '{"word":"PALC"}'
{"reverse_word":"CLAP"}
```

**Get release**

```sh
curl http://127.0.0.1:8080/ -X GET
```

```sh
curl -k reverse-default.apps.cluster-1234.example.com -X GET
```

**Get Health**

```sh
curl http://127.0.0.1:8080/health -X GET
```

```sh
curl -k reverse-default.apps.cluster-1234.example.com/health -X GET
```
