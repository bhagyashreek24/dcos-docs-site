
## Block Device / Storage

### Disk Recommendations

Spinnaker performs best when using disks with fast read and write patterns.

We recommend the following:

1. Always prefer locally-attached storage. Remote storage adds points of failure, add latency/overhead to block requests and are more complicated to troubleshoot.  
2. For better performance, use Solid-State Disks vs. Spinning disks or allocate more memory to cache more data, reducing the use of disks.
