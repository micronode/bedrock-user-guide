[principle of least privilege]: https://en.wikipedia.org/wiki/Principle_of_least_privilege

[Docker]: https://docker.com
[Terraform]: https://terraform.io
[Terraform Cloud]: https://app.terraform.io
[Cloudformation]: https://aws.amazon.com/cloudformation/
[Terragrunt]: https://github.com/gruntwork-io/terragrunt
[Astro]: https://github.com/uber/astro

[Introduction]: #introduction
[Security]: #security
[Resilience]: #resilience
[Efficiency]: #efficiency

#### Table of Contents

1. [Introduction - What is Bedrock?][Introduction]
2. [Security][Security]
3. [Resilience][Resilience]
4. [Efficiency][Efficiency]


## Introduction

Bedrock is a tool for provisioning infrastructure and services in a portable and consistent way.
Bedrock provides Terraform-based blueprints and a collection of fine-grained roles to assist with maintaining 
sprawling infrastructure and services across multiple platforms. 

When we design modern computing architectures it is important to consider **[Security]**, 
**[Resilience]** and **[Efficiency]** as equally important concerns. As we evolve each of these concerns within our solutions we find that they are not mutually
exclusive, but rather complement and feed into each other. This is especially true with public Cloud architectures

## Security

Security is a concern that must be recognised and addressed throughout the entire architecture lifecycle, from inception to build to operation. It is equally
important, and especially with public Cloud platfrorms, that security permeates the entire solution and is not just focused on the account perimiter.

Role-based access control (RBAC) allows us to restrict actors to the minimum required permissions, which is commonly 
referred to as the [principle of least privilege], and is the basis for the architectural blueprints provided by 
Bedrock.

## Resilience

TBD.

## Efficiency

Efficient use of resources has become a primary focus as more workloads are deployed into "pay for what you use" platforms such as public Cloud. However cost
reduction is not the only benefit of optimized architectures, as it also feeds into other concerns such as [Security] and resource management.

The key focus areas of Bedrock relating to efficiency include:

* Architectural Design - optimal architecturs for Cloud-native applications
* Cost Projection - cost budgeting vs actual
* Cost Allocation - tracking and tagging resources
* Compliance - pre-deployment checks and governance


## References

### Terraform

Bedrock is build on top of the functionality provided by [Terraform] and [Terraform Cloud] to
facilitate a simple, secure and consistent development and provisioning workflow.
 
