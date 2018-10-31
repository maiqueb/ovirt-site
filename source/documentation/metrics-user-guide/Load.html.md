# CPU Load Average Metrics

CPU load represents CPU contention, that is, the average number of schedulable processes at any given time. This is reported as an average value for all CPU cores on the host. Each CPU core can only execute one process at a time. Therefore, a CPU load average above 1.0 indicates that the CPUs have more work than they can perform, and the system is overloaded.

CPU load is reported over short term (last one minute), medium term (last five minutes) and long term (last fifteen minutes). While it is normal for a host's short term load average to exceed 1.0 (for a single CPU), sustained load average above 1.0 on a host may indicate a problem.

On multi-processor systems, the load is relative to the number of processor cores available. The "100% utilization" mark is 1.00 on a single-core, 2.00 on a dual-core, 4.00 on a quad-core system.

Red Hat recommends looking at CPU load in conjunction with [CPU Metrics](../CPU).

The following table describes the CPU load metrics reported by the **Load** plugin.

**CPU Load Average Metrics**

| Metric Name | Description |
|-
| collectd.load.load.longterm |Average number of schedulable processes per CPU core over the last 15 minutes. A value above 1.0 indicates the system was overloaded during the last 15 minutes. |
| collectd.load.load.midterm |Average number of schedulable processes per CPU core over the last five minutes. A value above 1.0 indicates the system was overloaded during the last 5 minutes. |
| collectd.load.load.shortterm |Average number of schedulable processes per CPU core over the last one minute. A value above 1.0 indicates the system was overloaded during the last minute. |

**Additional Values**

* **collectd.plugin:** Load
* **collectd.type:** load
* **collectd.type_instance:** None
* **collectd.plugin_instance:** None
* **ovirt.entity:** host
* **ovirt.cluster.name.raw:** *The cluster's name*
* **ovirt.engine_fqdn.raw:** *The Manager's FQDN*
* **hostname:** *The host's FQDN*
* **ipaddr4:** *IP address*
* **interval:** 10
* **collectd.dstypes:** [Guide](../Gauge)

