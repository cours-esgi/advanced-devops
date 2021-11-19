## FinOps

----

### Total Cost of Ownership (TCO)

Calculate accurately

* Cost of hardware and software (licences)
* Cost of outages and unavailability
* Cost of maintenance
* Cost of people

----

### Total Cost of Ownership (TCO)

* Eletrical power
* Location of datacenters
* Installation costs
* Maintenance costs

----

### Organization

Rule them all

Get together two world not affiliated : Finance and Operations

Can be applied to any organization, on public cloud or on-premises

----

### Organization

Structure
* A central organization that will lead the strategic vision of the company
* Gather technical and projects needs to drive architecture and use of best services
  * Dashboards and reports
  * Don't duplicate the effort
  * Centralized cost dashboards
* Control which services can be used
* A steering committee to define finops KPI to follow with all the stakeholders (financial, architets, project managers, etc)
* Challenge process to optimize the cost of ownership

----

### Organization

* Setup best practices like tagging
  * Drilldown
  * Fined-grained monitoring costs
  * Can be affected by BU / projects / etc.

----

### Share

Streamline the shared services between the teams to improve asset quality

Factor development effort by using innersourcing

Facilitate maintainance of code (for example reducing the patch time of systems)

----

### Share

Apply best practices uniformly, it reduces maintenance time and cost

* Common templates (IAM, Security groups, Cloudformation, etc.)
* Common security rules (MFA, password strength, roles, etc.)
* PSSI centralization

----

### Share

Follow common language for all the teams

For example:
  * Infrastructure: Terraform or Cloudformation?
  * Frontend language: React, Angular, Vue?

----

### Share

Ensure formation plans and tech watch

Maybe benefits new projects by been accelerated

Make POCs to test new solutions

----

### Shared responsibilities

In a Finops approach, it's important to cut hidden costs by monitor costs by projects.

We empower the teams. We can't have costs without knowing what we are doing.

We can create reports around 4 criteria:
* Reliability
* Business impact
* Resiliency
* Cost

----

### Rightsizing

Rightsizing is a process to size the architecture to adapt to real needs at a given time.

"As a service" enables to subscribe only what we need, the smallest size, the smallest number

It enables also to accelerate compared to a ticketing system (on average 6 weeks)

No oversizing

----

### Rightsizing

It can be difficult to estimate the cost of an application

We can leverage on tools like:
* Apptio
  * Business oriented reports
  * Optimization paths
* CloudCheckr
  * Centralize resources
  * Security best practices
  * Hints to densify or optimize infrastructure
* Cloudeasier
  * Predictable cost comparing on-premises and cloud
  * Warning: changing cloud provider has a cost
  * Warning: changing architecture has a cost

----

### Rightsizing

We can cut costs by removing unused resources

We can chose types of instances according to the needs, like burstable instances

Upfront can cut by 70% the cost associated to an application

DevOps-as-Code: infrastructure deployment, apps deployment

----

### Rightsizing

Environments:
  * Dev: fully automated, only when needed, destroyed after use
  * Test: fully automated, only when needed, destroyed after use, iso prod
  * Int: fully automated, only when needed, shutdown when not in use, can use serverless services
  * Preprod: fully automated, shutdown when not in use, apy only for data storage
  * Prod: automated and scalable

----

### High availability

Don't reinvent the wheel

We must ask ourselves the question of the capacity of the services to meet the business need

We must not forget high availability / scalability
  * We don't want to be called to tell us that the application is no longer available/slow...

----

### 6R approach

* Rehost (lift and shift)
* Replaftorm ("lift, tinker and shift")
  * Minor modifications
* Repurchase
  * Add services
* Refactor or rearchitect
  * Most flexible solution
  * Most expensive solution
* Retire
  * Should we continue to pay?
* Retain
  * Can we keep / reuse what we already have?

----

### Microservices

* Decouple applications to maintainable sizes and to avoid them becoming unmaintainable
* Scale only used services: less CPU or RAM consumed
* Use of languages suitable for processing 
* Distributed processing (for example in pySpark)
* Use of available managed services

----

### Use containers

Densify apps number on a server

Scaling "de facto": apps must be designed for (example: stateless services)

----

### Use serverless services

For example, use a JAMStack for a website
  * Hosted on a bucket
  * Statically built
  * Can support high throughput

Use REST API

Use managed services
  * ~70% less time to provision
  * ~45% to ~80% cost reduction on maintanance

----

## Takeways

* Structured organization
* Challenged architecture
* Appropriate services and resources
* Monitor TCO
