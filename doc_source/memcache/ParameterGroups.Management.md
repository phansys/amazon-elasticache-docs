# Parameter Management<a name="ParameterGroups.Management"></a>

Parameters are grouped together into named parameter groups for easier parameter management\. A parameter group represents a combination of specific values for the parameters that are passed to the engine software during startup\. These values determine how the engine processes on each node will behave at runtime\. The parameter values on a specific parameter group apply to all nodes that are associated with the group, regardless of which cluster they belong to\.

To fine tune your cluster's performance, you can modify some parameter values or change the cluster's parameter group\.

**Constraints**
+ You cannot modify or delete the default parameter groups\. If you need custom parameter values, you must create a custom parameter group\.
+ The parameter group family and the cluster you're assigning it to must be compatible\. For example, if your cluster is running Memcached version 1\.4\.8, you can only use parameter groups, default or custom, from the Memcached 1\.4 family\.

  The parameter group family and the cluster you're assigning it to must be compatible\. For example, if your cluster is running Redis version 3\.2\.10, you can only use parameter groups, default or custom, from the Redis3\.2 family\.
+ If you change a cluster's parameter group, the values for any conditionally modifiable parameter must be the same in both the current and new parameter groups\.
+ When you make a change to a cluster's parameters, either by changing the cluster's parameter group or by changing a parameter value in the cluster's parameter group, the changes are applied to the cluster either immediately or after the cluster is restarted\. To determine when a particular parameter change is applied, see the **Changes Take Effect** column in the tables for [Memcached Specific Parameters](ParameterGroups.Memcached.md)\. For information on rebooting a cluster, see [Rebooting a Cluster](Clusters.Rebooting.md)\.