## SRE

----

### Let's get back to DevOps

* DevOps is a set of practices that works to automate and integrate the processes between sotware development and IT teams, so they can build, test and release software faster and more reliably. - Atlassian
* DevOps is the combination of cultural philosophies, practices and tools that increase and organization's ability to deliver applications and services at high velocity. - AWS
----

### Let's get back to DevOps

* DevOps is the union of people, process and product to enable continuous delivery of value to our end users. - Microsoft
* DevOps is a set of practices that combines software development (Dev) and IT (Ops) to deliver software that is reliable, efficient and scalable. - Wikipedia

----

### So what is SRE?

SRE stands for Site Reliability Engineering

Born in 2003 at Google, prior to DevOps (2008)

Is "what happens when a software engineer is tasked with what used to be called oprations" - Ben Treynor, Google's SRE founder

Reliability is "the most important feature of any system" - Google

----

### What is the terminology for SRE?

* Service Level Indicator (SLI) - Quantifiable measure of service reliability
* Service Level Objective (SLO) - Reliability target for an SLI
* Service Level Agreement (SLA) - Agreement between a customer and a provider of a service
* Error budget - The maximum number of errors that can occur before a service is considered to be in a degraded state

----

### From here, what is an appropriate objective?

* Not 100%
  * A bit high, isn't it?
  * "100% is the wrong reliablity target for basically anything" - Google
* "Everything fails all the time" - Werner Vogels, CTO Amazon.com

----

### From here, what is an appropriate objective?

The minimum that makes standard customer happy

SLOs should capture the performance and availability levels that, if barely met, would keep the typical customer of a service happy.

* "Meets SLO targets" => happy customers
* "Sad customers" => misses SLO targets

----

### Error budget

Define SLO means accepting to fail

* The number of failures of the time allocated to failure is your "Error budget"
* It reflects the balance between innovation and stability
* This is the contract between Dev and Ops
* Calculated over a set of rolling windows
* Consume it wisely

----

### How to define my SLIs?

SLI = (good events / valid events) * 100 %

----

### How to define good SLIs?

* Four golden signals
  * Latency
  * Traffic
  * Errors
  * Saturation

----

### Latency

The time it takes to service a request. It’s important to distinguish between the latency of successful requests and the latency of failed requests. For example, an HTTP 500 error triggered due to loss of connection to a database or other critical backend might be served very quickly; however, as an HTTP 500 error indicates a failed request, factoring 500s into your overall latency might result in misleading calculations. On the other hand, a slow error is even worse than a fast error! Therefore, it’s important to track error latency, as opposed to just filtering out errors.

----

### Traffic

A measure of how much demand is being placed on your system, measured in a high-level system-specific metric. For a web service, this measurement is usually HTTP requests per second, perhaps broken out by the nature of the requests (e.g., static versus dynamic content). For an audio streaming system, this measurement might focus on network I/O rate or concurrent sessions. For a key-value storage system, this measurement might be transactions and retrievals per second.

----

### Errors

The rate of requests that fail, either explicitly (e.g., HTTP 500s), implicitly (for example, an HTTP 200 success response, but coupled with the wrong content), or by policy (for example, "If you committed to one-second response times, any request over one second is an error").

----

### Errors

Where protocol response codes are insufficient to express all failure conditions, secondary (internal) protocols may be necessary to track partial failure modes. Monitoring these cases can be drastically different: catching HTTP 500s at your load balancer can do a decent job of catching all completely failed requests, while only end-to-end system tests can detect that you’re serving the wrong content.

----

### Saturation

How "full" your service is. A measure of your system fraction, emphasizing the resources that are most constrained (e.g., in a memory-constrained system, show memory; in an I/O-constrained system, show I/O). Note that many systems degrade in performance before they achieve 100% utilization, so having a utilization target is essential.

----

### Saturation

In complex systems, saturation can be supplemented with higher-level load measurement: can your service properly handle double the traffic, handle only 10% more traffic, or handle even less traffic than it currently receives? For very simple services that have no parameters that alter the complexity of the request (e.g., "Give me a nonce" or "I need a globally unique monotonic integer") that rarely change configuration, a static value from a load test might be adequate. As discussed in the previous paragraph, however, most services need to use indirect signals like CPU utilization or network bandwidth that have a known upper bound. ----

----

### Saturation

Latency increases are often a leading indicator of saturation. Measuring your 99th percentile response time over some small window (e.g., one minute) can give a very early signal of saturation.
Finally, saturation is also concerned with predictions of impending saturation, such as "It looks like your database will fill its hard drive in 4 hours."

----

### No more than 3 to 5 SLIs per user journey

For example:
  * Request / Response
    * Availability
    * Latency
    * Quality

----

### No more than 3 to 5 SLIs per user journey

  * Data processing
    * Coverage
    * Correctness
    * Freshness
    * Throughput

----

### No more than 3 to 5 SLIs per user journey

  * Storage
    * Throughput
    * Latency

----

### Then, drill down the mesurement strategies

For example:
  * Application-level metrics
  * Logs processing
  * Frontend infrastructure metrics
  * Synthetic client data
  * Client-side instrumentation

----

### Adapt wisely your strategy to slowly burn your error budget

* Pilot
  * Budget
  * Pace
* Target
  * Users
  * SLO

----

### Adapt wisely your strategy to slowly burn your error budget

* Automate
  * Deployment
  * Rollback
* Monitor
  * Logs
  * Metrics
  * SLO