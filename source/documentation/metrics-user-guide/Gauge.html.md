# Gauge and Derive Data Source Types

Each metric includes a *collectd.dstypes* value that defines the data source's type:

* **Gauge**: A gauge value is simply stored as-is and is used for values that may increase or decrease, such as the amount of memory used. 

* **Derive**: These data sources assume that the change of the value is interesting, i.e., the derivative. Such data sources are very common for events that can be counted, for example the number of disk read operations. The total number of disk read operations is not interesting, but rather the change since the value was last read. The value is therefore converted to a rate using the following formula:

  ```
  rate = value(new)-value(old)\
          time(new)-time(old) 
  ```

**Note:** If value(new) is less than value (old), the resulting rate will be negative. If the minimum value to zero, such data points will be discarded.


