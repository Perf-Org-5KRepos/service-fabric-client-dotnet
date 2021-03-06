# Get-SFClusterHealth
Gets the health of a Service Fabric cluster.
## Description

Use EventsHealthStateFilter to filter the collection of health events reported on the cluster based on the health 
state.
                Similarly, use NodesHealthStateFilter and ApplicationsHealthStateFilter to filter the collection of 
nodes and applications returned based on their aggregated health state.



## Optional Parameters
#### -NodesHealthStateFilter

Allows filtering of the node health state objects returned in the result of cluster health query
                    based on their health state. The possible values for this parameter include integer value of one 
of the
                    following health states. Only nodes that match the filter are returned. All nodes are used to 
evaluate the aggregated health state.
                    If not specified, all entries are returned.
                    The state values are flag-based enumeration, so the value could be a combination of these values 
obtained using bitwise 'OR' operator.
                    For example, if the provided value is 6 then health state of nodes with HealthState value of OK 
(2) and Warning (4) are returned.
                    
                    - Default - Default value. Matches any HealthState. The value is zero.
                    - None - Filter that doesn't match any HealthState value. Used in order to return no results on a 
given collection of states. The value is 1.
                    - Ok - Filter that matches input with HealthState value Ok. The value is 2.
                    - Warning - Filter that matches input with HealthState value Warning. The value is 4.
                    - Error - Filter that matches input with HealthState value Error. The value is 8.
                    - All - Filter that matches input with any HealthState value. The value is 65535.



#### -ApplicationsHealthStateFilter

Allows filtering of the application health state objects returned in the result of cluster health
                    query based on their health state.
                    The possible values for this parameter include integer value obtained from members or bitwise 
operations
                    on members of HealthStateFilter enumeration. Only applications that match the filter are returned.
                    All applications are used to evaluate the aggregated health state. If not specified, all entries 
are returned.
                    The state values are flag-based enumeration, so the value could be a combination of these values 
obtained using bitwise 'OR' operator.
                    For example, if the provided value is 6 then health state of applications with HealthState value 
of OK (2) and Warning (4) are returned.
                    
                    - Default - Default value. Matches any HealthState. The value is zero.
                    - None - Filter that doesn't match any HealthState value. Used in order to return no results on a 
given collection of states. The value is 1.
                    - Ok - Filter that matches input with HealthState value Ok. The value is 2.
                    - Warning - Filter that matches input with HealthState value Warning. The value is 4.
                    - Error - Filter that matches input with HealthState value Error. The value is 8.
                    - All - Filter that matches input with any HealthState value. The value is 65535.



#### -EventsHealthStateFilter

Allows filtering the collection of HealthEvent objects returned based on health state.
                    The possible values for this parameter include integer value of one of the following health states.
                    Only events that match the filter are returned. All events are used to evaluate the aggregated 
health state.
                    If not specified, all entries are returned. The state values are flag-based enumeration, so the 
value could be a combination of these values, obtained using the bitwise 'OR' operator. For example, If the provided 
value is 6 then all of the events with HealthState value of OK (2) and Warning (4) are returned.
                    
                    - Default - Default value. Matches any HealthState. The value is zero.
                    - None - Filter that doesn't match any HealthState value. Used in order to return no results on a 
given collection of states. The value is 1.
                    - Ok - Filter that matches input with HealthState value Ok. The value is 2.
                    - Warning - Filter that matches input with HealthState value Warning. The value is 4.
                    - Error - Filter that matches input with HealthState value Error. The value is 8.
                    - All - Filter that matches input with any HealthState value. The value is 65535.



#### -ExcludeHealthStatistics

Indicates whether the health statistics should be returned as part of the query result. False by default.
                    The statistics show the number of children entities in health state Ok, Warning, and Error.



#### -IncludeSystemApplicationHealthStatistics

Indicates whether the health statistics should include the fabric:/System application health statistics. False by 
default.
                    If IncludeSystemApplicationHealthStatistics is set to true, the health statistics include the 
entities that belong to the fabric:/System application.
                    Otherwise, the query result includes health statistics only for user applications.
                    The health statistics must be included in the query result for this parameter to be applied.



#### -ServerTimeout

The server timeout for performing the operation in seconds. This timeout specifies the time duration that the client 
is willing to wait for the requested operation to complete. The default value for this parameter is 60 seconds.



