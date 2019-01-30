# Pumba Helm Chart

This repository contains the **Pumba Helm Chart** to deploy [Pumba](https://github.com/alexei-led/pumba) to [Kubernetes](https://kubernetes.io/)

## Install Helm

Get the latest [Helm release](https://github.com/kubernetes/helm#install).

## Install Chart

1. Clone the repository:

   ```console
   git clone https://github.com/iamShantanu101/pumba-helm
   ```

2. Modify the values in `values.yaml` as per your needs.

3. Initiate chaos with Pumba by running:
   ```console
   helm install ./pumba \
      --name pumba \
      --namespace pumba \
      --values=./pumba/values.yaml
   ```

For more detailed instructions, see the chart's documentation [here](https://github.com/iamShantanu101/pumba-helm/blob/master/pumba/README.md).

## Reporting Issues

Please report all issues via github issues [here](https://github.com/iamShantanu101/pumba-helm/issues).

## Credits

Big thanks to [Pumba](https://github.com/alexei-led/pumba) (@alexei-led) for creating Pumba.

