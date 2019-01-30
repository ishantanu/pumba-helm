# Pumba Helm Chart

## Prerequisites

* Kubernetes with `extensions/v1beta1` available

## Configuration

By default this chart will initiate the chaos by deploying [Pumba](https://github.com/alexei-led/pumba) CE tool.

The following table lists common configurable parameters of the chart and
their default values. See [values.yaml](https://github.com/iamShantanu101/pumba-helm/blob/master/pumba/values.yaml) for all available options.

|       Parameter                        |           Description                       |                         Default                     |
|----------------------------------------|---------------------------------------------|-----------------------------------------------------|
| `image.pullPolicy`                     | Container pull policy                       | `Always`                                            |
| `image.repository`                     | Container image to use                      | `gaiaadm/pumba`                                   |
| `image.tag`                            | Container image tag to deploy               | `master`                                            |
| `nodeSelector`                         | Map of node labels for pod assignment       | `{}`                                                |
| `tolerations`                          | List of node taints to tolerate             | `[]`                                                |
| `affinity`                             | Map of node/pod affinities                  | `{}`                                                |
| `pumbaSelfKill`                      | Prevent Pumba from killing itself           | `false`                                             |
| `pumba.args`                  | Supply arguments to initiate chaos via Pumba (by default initiates a random chaos)           | `[--random, --interval, "3m", kill, --signal, "SIGKILL"]`                                             |
| `resources`                      | CPU/memory resource requests/limits           |                                            |

Specify each parameter using the `--set key=value[,key=value]` argument to
`helm install`.

## Installation

1. Clone the repository:

   ```shell
   git clone https://github.com/iamShantanu101/pumba-helm
   ```

2. Modify the values in `values.yaml` as per your needs.

3. Initiate chaos with Pumba by running:
   ```shell
   helm install ./pumba \
      --name pumba \
      --namespace pumba \
      --values=./pumba/values.yaml
   ```

## Uninstall

```shell
helm delete pumba
```

To delete the deployment and its history:
```shell
helm delete --purge pumba
```
