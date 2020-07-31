# Blueprint Provisioning

## Prerequisites

Before provisioning a new blueprint instance you should decide which provisioning model to use.

### Local

Local provisioning is supported by three backend types: local, S3 and remote.

A local backend has no prerequisites, but is also not recommended due to potential for data loss.

An S3 backend requires an AWS account configured via environment variables or local configuration file.

A remote backend for local execution requires terraform cloud file or environment-based configuration.

In addition local execution requires credentials for target environments, which may be the same credentials used for the backend.

In fact if you require provisioning to multiple different accounts it is advisable to use a remote execution model due to limitations of local execution with multiple credentials/accounts.

### Remote

Remote execution is supported by terraform cloud via standardised execution environments. Only the remote backend type is supported by this model.

A remote backend for remote execution only requires terraform cloud credentials configured via file or environment variables.

Note that there are limitations on remote execution of blueprints that contain local-exec provisioning, which also needs to be taken into consideration when deciding on the execution model.

## Commands

### Backend

Configure the blueprint backend using the backend command:

`$ blueprint <id> backend <local|S3|remote> [options]`

An S3 backend requires a bucket name for state.

A remote backend requires a terraform cloud organisation and a prefix for cloud workspaces.

### Workspace

You can use workspaces to manage multiple instances of the same blueprint. This is essential when using a remote backend as the local workspace is used to define the cloud workspaces.

`$ blueprint <id> workspace new <name>`

### Init

After configuration of the backend and workspace, initialisation of the blueprint instance will download required plugins and modules for execution.

`$ blueprint <id> init`

### Plan

A blueprint plan is used to identify required input variables and preview the changes made by provisioning. If you know the required input variables you may specify on the command line.

`$ blueprint <id> plan [input vars]`

### Apply

A blueprint instance is provisioned using the apply command. As with the plan command input variables may be specified to override defaults.

`$ blueprint <id> apply [input vars]`

### Multiple instances

By default a single blueprint instance is created with the"default" tag. You can create multiple instances of a blueprint by using the"tag" option supported by all blueprint commands.

`$ blueprint --tag <tag> <id> <command>`

 
   