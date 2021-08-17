# Implementing Service Health Checks
This page provides patterns for how service health check may be implemented.

## Overiew

Health checks are a critical component of responsive, highly available services. Health checks are the first line of defence when detecting and responding to service interruption, and as such need to be sophisticated enough to detect and report on anything that may be perceived as an interruption to service.

## TCP vs HTTP Health Checks

Some platforms that use health checks to determine the state of a deployed service will provide the option for TCP or HTTP health checks. TCP health checks will simply test for an open TCP port (e.g. port 80 for web services), and assume the service is healthy.

Whilst  TCP health checks may be an option for non-HTTP services, as this approach alleviates the need for a dedicated health check endpoint, it is almost always not an optimal approach as there could be a number of reasons why the port is open but the service is still unhealthy.

Alternatively, HTTP health checks may be used with the default service endpoint (for simple, unauthenticated services), but ideally should have a specific health check endpoint that can provide more sophisticated health reporting.

## Status Response

Typically a health check is implemented as an HTTP endpoint that responds with appropriate HTTP status codes when invoked. Some common status codes may include:

* 200 - Service is healthy
* 503 - Service is down
* 504 - Backing services unreachable
* …

