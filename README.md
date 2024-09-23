# Cloudfairy

## Prequisites
- Kubernetes cluster
- kubectl with active context

## Installation
```bash
kubectl apply -f https://raw.githubusercontent.com/cloud-fairy/kubernetes/refs/heads/main/install-cloudfairy.yaml
```

## User Interface
```bash
kubectl get pods -n cloudfairy

# exptected output
# NAME                                     READY   STATUS              RESTARTS   AGE
# cloudfairy-controller-79d7755f98-v6xmm   0/1     Running             0          62s

kubectl port-forward -n cloudfairy pods/cloudfairy-controller-79d7755f98-v6xmm 1337:1337

# expected output
# Forwarding from 127.0.0.1:1337 -> 1337
# Forwarding from [::1]:1337 -> 1337
```

Browse to http://127.0.0.1:1337
Create a new project, and click "edit".
Once you are in the designer screen, you might want to add your own components, or install the demo component library.

If you wish to install your own component library, you can click the "dots" menu button on the left panel, and choose "Import component..."
Fill in the url pointing to a zip file containing the manifests, and import.

Reload the page and start working on your project.
