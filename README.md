# kubernetes-persistent-disk-setup
How to mount a persistent disk in multiple pods. (when you pods want to access files inside pd)

I feel like it is not a lot of explaination in this type of uses, it took me a long unecessary time to get this all sort out. So I feel like helping others if they want to use persistent disk in the same way.

This is for people are doing project with huge pod container.

You create and put some of the files in the persistent disk. (I will not give how to create a disk since there are a lot of ways. Very easy to search online)

Because you want to mount the disk for multiple pods so this is a great way.

1. create a persistent volume.

2. create a StorageClass.

3. create a persistent disk claim.

4. create a pod and mount the disk.

5. Use "kubectl apply -f persistentvolume.yaml"
       "kubectl apply -f StorageClass.yaml"
       "kubectl apply -f PersistentVolumeClaim.yaml"
       "kubectl apply -f pd-pod.yaml"

Reference:
1. https://kubernetesio/docs/tasks/configure-pod-container/configure-persistent-volume-storage/

2. https://cloud.google.com/kubernetes-engine/docs/concepts/persistent-volumes
