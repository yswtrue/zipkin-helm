# zipkin-helm
A helm chart for zipkin

## usage

### Adding the repo 

`helm repo add zipkin-helm https://financial-times.github.io/zipkin-helm/docs`

### Installing

`helm install -f my-cassandra-config.yaml https://financial-times.github.io/zipkin-helm/docs/zipkin-helm-0.1.1.tgz`

## values

Example

```
cassandra:
  username: zipkinuser
  password: my-super-secret-password
  contactPoints: cassandra-1.me.com,cassandra-2.me.com

ingress:
  host: zipkin.example.com

configmap:
  localdc:
    name: cassandra # use this notation if you want to reuse values from existing configmaps, this takes precedence over the .cassandra field
    key: local.dc
```