# Get-SFDeployedServiceReplicaInfoList
Gets the list of replicas deployed on a Service Fabric node.
## Description

Gets the list containing the information about replicas deployed on a Service Fabric node. The information include 
partition ID, replica ID, status of the replica, name of the service, name of the service type, and other information. 
Use PartitionId or ServiceManifestName query parameters to return information about the deployed replicas matching the 
specified values for those parameters.



## Required Parameters
#### -NodeName

The name of the node.



#### -ApplicationId

The identity of the application. This is typically the full name of the application without the 'fabric:' URI scheme.
                    Starting from version 6.0, hierarchical names are delimited with the "~" character.
                    For example, if the application name is "fabric:/myapp/app1", the application identity would be 
"myapp~app1" in 6.0+ and "myapp/app1" in previous versions.



## Optional Parameters
#### -PartitionId

The identity of the partition.



#### -ServiceManifestName

The name of a service manifest registered as part of an application type in a Service Fabric cluster.



#### -ServerTimeout

The server timeout for performing the operation in seconds. This timeout specifies the time duration that the client 
is willing to wait for the requested operation to complete. The default value for this parameter is 60 seconds.



