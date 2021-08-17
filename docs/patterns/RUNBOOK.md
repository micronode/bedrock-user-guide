# Implementing Runbooks
This page provides information on different types of runbook and when to use them.

## Overview

A Runbook is essentially a series of repeatable steps in response to an event or issue identified in a system architecture. Runbooks may be manual or automated, depending on the activity being performed.

## Manual Runbooks

A manual runbook is esentially a series of instructions for a human operator to perform. This could include things like restarting a container or virutal machine when a service is unresponsive, or isolating a component when a security breach has been detected.

## Automated Runbooks

Ideally we would like to have entirely automated responses to system issues, and this may be something that is evolved over time. For example, after establishing a manual runbook for restarting a service, we may be able to translate this into an automated process.
