# garden-kube-apiserver
This helmcharts helps to deploy an kubernetes apiserver to be extended by the gardener-apiserver. This is mostly a clone from the garden-kube-apiserver helmchart from garden-setup. Two minor differences are the ability to set custom annotations for the ingress of the apiserver and that you can tell the apiserver to place a bootstrap kubeconfig for a gardenlet.

## ingress annotation
Use `ingress.annotations` to add custom annotations to the ingress of the apiserver.
## gardenlet bootstrap kubeconfig
Set `gardenletBootstrap.createToken` to true to place a bootstrap kubeconfig. You can set the values of the token and the secret via `gardenletBootstrap.token` and `gardenletBootstrap.secret`. The ca can be set via `tls.kubeAPIServer.ca.crt`.
