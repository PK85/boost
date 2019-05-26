# boost

## why
**Question**: *Find a way how to configure k8s that in case of some pods ends with CrashLoopBackOff (because some required dependencies are still not running)  kubelet will not restart them with an exponential back-off delay (10s, 20s, 40s …)*
**Answer**: *Just write a controller that watches the api for pods in CrashLoopBackoff and deletes them.*

## stack
- go 1.12
- go modules 
- kubebuilder
