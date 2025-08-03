## NodeAffinity

Types:
1.	**requiredDuringSchedulingIgnoredDuringExecution**: The pod will only be scheduled on nodes that strictly match the specified labels, but it won’t be evicted if those labels change later.

2.	**preferredDuringSchedulingIgnoredDuringExecution**: The scheduler will try to place the pod on a node that matches the preferred labels, but will fall back to others if needed.

3.	**requiredDuringSchedulingRequiredDuringExecution**: This type is only valid for pod affinity rules, where the condition must be true both at scheduling time and throughout the pod’s lifetime.
