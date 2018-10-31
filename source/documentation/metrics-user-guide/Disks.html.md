# Disk Operation Metrics

Disk operation metrics are reported per physical disk on the host, and per partition.

The following table describes the disk operation metrics reported by the *Disk* plugin.

**Disk Operation Metrics**

|Metric Name |Description |collectd.dstypes|
|-
| collectd.disk.disk_ops.read |The number of disk read operations. |[Derive](../Derive)|
| collectd.disk.disk_ops.write |The number of disk write operations. |[Derive](../Derive)|
| collectd.disk.disk_merged.read |The number of disk reads that have been merged into single physical disk access operations. In other words, this metric measures the number of instances in which one physical disk access served multiple disk reads. The higher the number, the better. |[Derive](../Derive)|
| collectd.disk.disk_merged.write |The number of disk writes that were merged into single physical disk access operations. In other words, this metric measures the number of instances in which one physical disk access served multiple write operations. The higher the number, the better. |[Derive](../Derive)|
| collectd.disk.disk_time.read |The average amount of time it took to do a read operation, in milliseconds. |[Derive](../Derive)|
| collectd.disk.disk_time.write |The average amount of time it took to do a write operation, in milliseconds. |[Derive](../Derive)|
| collectd.disk.pending_operations |The queue size of pending I/O operations. |[Gauge](../Gauge)|
| collectd.disk.disk_io_time.io_time | The time spent doing I/Os in milliseconds. This can be used as a device load percentage, where a value of 1 second of time spent represents a 100% load.  |[Derive](../Derive)|
| collectd.disk.disk_io_time.weighted_io_time |A measure of both I/O completion time and the backlog that may be accumulating.  |[Derive](../Derive)|

**Additional Values**

* **collectd.plugin:** Disk
* **collectd.type_instance:** None
* **collectd.plugin_instance:** *The disk's name*
* **ovirt.entity:** host
* **ovirt.cluster.name.raw:** *The cluster's name*
* **ovirt.engine_fqdn.raw:** *The Manager's FQDN*
* **hostname:** *The host's FQDN*
* **ipaddr4:** *IP address*
* **interval:** 10

