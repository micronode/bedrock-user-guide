# Serverless Architectures
This page provides information on the ways to adopt serverless architectures and minimise the number of self-managed resources.

## Overview

Serverless computing is essentially using managed infrastructure to deploy services and resources. This may include compute workloads, data persistence and integration tooling that may traditionally have been self-hosted on virtual machines.

## Compute
Traditionally compute resources have required virtual machines (VMs) for hosting software applications that provide a service. Increasingly there are more serverless options for hosting and running such applications without VMs. Platforms offerings such as Container-as-a-service (CaaS) and Function-as-a-service (FaaS) provide the ability to deploy varied compute resources without a need to maintain the underlying VM infrastructure.

## Resources
Often static resources don't need a dedicated compute resource to deliver as they are simply files that require delivery to the requestor. As such we can often use file storage services and content delivery networks (CDNs) to serve static resources without any intermediate compute resources. 

## Data
Serverless databases are now quite common in both traditional Relational and NoSQL variants.

