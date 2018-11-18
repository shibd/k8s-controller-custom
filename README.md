## Running

```
$ godep restore -v
$ go build -o network-controller
$ ./network-controller -kubeconfig=$HOME/.kube/config -alsologtostderr=true
```

## Usage

You should create the CRD of Network first:

```
$ kubectl apply -f crd/network.yaml
```

You can then trigger an event by creating a Network API instance:

```
$ kubectl apply -f example/example-network.yaml
```

CURD the Network API instance, and check the logs of controller. 
