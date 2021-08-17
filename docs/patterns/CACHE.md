# Caching service responses
This page highlights patterns and mechanism for caching data to alleviate load and improve performance.

## Overview

Caching is an important concept to improve the availability, responsiveness and efficiency of services. Many modern architectures are a distributed collection of many microservices, which means that communication between these services can a key bottleneck of performant systems. Caching provides a way to reduce the load on services responding to requests by using precalculated responses.

