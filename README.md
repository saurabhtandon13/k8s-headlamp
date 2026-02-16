# k8s-headlamp
This repository walk us through the installation of headlamp on the Kubernetes cluster

root@globalmachine /root/software/k8s-headlamp                                                                                                                                                                                                                                                                     main
⚡ helm repo add headlamp https://kubernetes-sigs.github.io/headlamp/
"headlamp" has been added to your repositories

root@globalmachine /root/software/k8s-headlamp                                                                                                                                                                                                                                                                     main
⚡ helm repo update
Hang tight while we grab the latest from your chart repositories...
...Successfully got an update from the "headlamp" chart repository
...Successfully got an update from the "nvidia" chart repository
...Successfully got an update from the "actions-runner-controller" chart repository
...Successfully got an update from the "kyverno" chart repository
Update Complete. ⎈Happy Helming!⎈

root@globalmachine /root/software/k8s-headlamp                                                                                                                                                                                                                                                                     main
⚡ helm repo list
NAME                            URL
nvidia                          https://helm.ngc.nvidia.com/nvidia
kyverno                         https://kyverno.github.io/kyverno/
actions-runner-controller       https://actions-runner-controller.github.io/actions-runner-controller
headlamp                        https://kubernetes-sigs.github.io/headlamp/

root@globalmachine /root/software/k8s-headlamp                                                                                                                                                                                                                                                                     main
⚡ vim README.md

root@globalmachine /root/software/k8s-headlamp                                                                                                                                                                                                                                                                     main
⚡ helm search repo headlamp
NAME                    CHART VERSION   APP VERSION     DESCRIPTION
headlamp/headlamp       0.40.0          0.40.0          Headlamp is an easy-to-use and extensible Kuber...

root@globalmachine /root/software/k8s-headlamp                                                                                                                                                                                                                                                                     main
⚡ helm pull headlamp/headlamp --untar
level=WARN msg="unable to find exact version; falling back to closest available version" chart=headlamp requested="" selected=0.40.0
Error: failed to untar: a file or directory with the name headlamp already exists

root@globalmachine /root/software/k8s-headlamp                                                                                                                                                                                                                                                                     main
⚡ ls -lart
total 20
drwxr-xr-x 12 root root 4096 Feb 10 07:08 ..
-rw-r--r--  1 root root  984 Feb 10 07:10 headlamp
-rw-r--r--  1 root root 2253 Feb 10 07:22 README.md
drwxr-xr-x  3 root root 4096 Feb 10 07:22 .
drwxr-xr-x  8 root root 4096 Feb 10 07:23 .git

root@globalmachine /root/software/k8s-headlamp                                                                                                                                                                                                                                                                     main
⚡ rm -rf headlamp

root@globalmachine /root/software/k8s-headlamp                                                                                                                                                                                                                                                                     main
⚡ helm pull headlamp/headlamp --untar
level=WARN msg="unable to find exact version; falling back to closest available version" chart=headlamp requested="" selected=0.40.0

root@globalmachine /root/software/k8s-headlamp                                                                                                                                                                                                                                                                     main
⚡

