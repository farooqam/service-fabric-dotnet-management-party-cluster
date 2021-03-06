---
services: service-fabric
platforms: dotnet
author: vturecek
---

# Azure Service Fabric Party Cluster

This sample application manages a set of Service Fabric clusters hosted on Azure, demonstrating basic management tasks. It keeps a working set of cluster metadata in a Reliable Dictionary to keep track of the party clusters, which are live running Service Fabric clusters in Azure. It knows when to create new ones, when to delete expired ones, when to scale the number of clusters out and back in depending on user activity, and all the other management tasks required to keep the party going.  

See the Party Cluster application live and try it for yourself at [http://aka.ms/tryservicefabric](http://aka.ms/tryservicefabric)

## Patterns and features

This application is a sample project that primarily demonstrates two management functions:

1.  How to use the Azure Resource Manager APIs to manage Azure Resource Groups to create Service Fabric clusters in Azure. 
2.  How to use Service Fabric management APIs to create and query Service Fabric applications.

The project also demonstrates a number of Service Fabric features and patterns for application development, including:


-  Stateful Reliable Services with Reliable Collections.
-  Dependency injection and unit testing with Reliable Services.
-  How to use Service Fabric configuration packages, both the built-in Settings.xml config and custom JSON configuration, with rolling updates without restarting services.
-  How to encrypt sensitive data in Service Fabric configuration packages.
-  Inter-service communication using the Service Fabric remoting stack.
-  Diagnostics with Elastic Search through ETW event sources.
-  How to write a stateless Web API front-end service.

