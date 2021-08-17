# Managing Secrets
This page outlines approaches for secrets management and integration with services.

## Overview

Secrets are a critical piece of system design, and are commonly used for integrating with backing services and other systems. Somewhat counter-intuitively, we should ultimately be trying to minimise the number of secrets we manage, as the most secure secrets are no secrets. But most systems will need some secrets and the following patterns highlight approaches for maintenance.

## Something you know vs are

You may be familiar with the multi-factor authentication model, whereby you typically provide at least two different kinds of authentication. This is often know as "something you know" (e.g. a password) and "something you have" (e.g. a temporary code from a code generator, SMS message, etc.).

On some platforms, such as public Cloud infrastructure, we can use a similar concept using service roles to identify specific services (i.e. "something you are"). If we can use the platform roles to identify services then we can often avoid secrets ("something you know"), thus minimising the risk of secrets management.

## When you need secrets

TBD.
