# Pumba Helm Chart

This repository contains the **Pumba Helm Chart** to deploy [Pumba](https://github.com/alexei-led/pumba) to [Kubernetes](https://kubernetes.io/)

## Install Helm

Get the latest [Helm release](https://github.com/kubernetes/helm#install).

## Install Charts

1. Add this Chart repo to Helm:

   ```console
   helm repo add pumba-helm https://github.com/iamShantanu101/pumba-helm
   ```

2. Copy the `values.yaml` file from the repo and modify it as per your needs.
3. Initiate chaos with Pumba by running:
   ```console
   helm install pumba-helm/pumba \
      --name pumba \
      --namespace pumba \
      --values=values.yaml
   ```

For more detailed instructions, see the chart's documentation [here](https://github.com/iamShantanu101/pumba-helm/blob/master/pumba/README.md).

## Reporting Issues

Please report all issues via github issues [here](https://github.com/iamShantanu101/pumba-helm/issues).

## Credits

Big thanks to [Pumba](https://github.com/alexei-led/pumba) (@alexei-led) for creating Pumba.

