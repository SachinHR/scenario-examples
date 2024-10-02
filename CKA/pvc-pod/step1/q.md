
> <strong>Useful Resources</strong>: [Persistent Volumes Claim](https://kubernetes.io/docs/concepts/storage/persistent-volumes/) , [Pod to Use a PV](https://kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage/)

For this question, please set this context (In exam, diff cluster name)

`kubectl config use-context kubernetes-admin@kubernetes`{{exec}}

<br>

A Kubernetes pod definition file named `nginx-pod-cka.yaml` is available. Your task is to make the following modifications to the manifest file:

* Create a Persistent Volume Claim (PVC) with the name `nginx-pvc-cka`. This PVC should request `80Mi` of storage from an existing Persistent Volume (PV) named `nginx-pv-cka` and Storage Class named`nginx-stc-cka`. Use the access mode `ReadWriteOnce`.
* Add the created `nginx-pvc-cka` PVC to the existing `nginx-pod-cka` POD definition.
* Mount the volume claimed by `nginx-pvc-cka` at the path `/var/www/html` within the `nginx-pod-cka` POD.
* Add tolerations with the key `node-role.kubernetes.io/control-plane` set to `Exists` and effect `NoSchedule` to the `nginx-pod-cka` Pod
* Ensure that the `my-pod-cka` POD is running and that the Persistent Volume (PV) is successfully `bound`.
