[Guaranteed]
Guaranteed components of the cluster require all containers within a pod((including init containers) to have a cpu limit=cpu request, and memory limit=memory rquest. Because of the strict requirements, applications must be known inside and out

Current:
  - kube-apiserver
TODO:
  - cilium

[Burstable]
Everything should have a limit on memory and be tuned as needed. CPU's should just be minimal requests and then get bumped up as applications show what they actually tend to consume
