## DevSecOps

----

### What Is DevSecOps?

DevSecOps refers to the integration of security practices into a DevOps software delivery model. Its foundation is a culture where development and operations are enabled through process and tooling to take part in a shared responsibility for delivering secure software.

The definition of DevSecOps Model, at a high-functioning level, is to integrate security objectives as early as possible in the lifecycle of software development. While security is “everyone’s responsibility,” DevOps teams are uniquely positioned at the intersection of development and operations, empowered to apply security in both breadth and depth.

----

### What Is the Difference Between DevOps and DevSecOps?

The difference between DevOps and DevSecOps is, to put it simply, the culture of shared responsibility. DevOps is a concept that has been talked about and written about for over a decade, and many definitions of DevOps have emerged. At its core, DevOps is an organizational paradigm that aligns development and operations practices as a shared responsibility.

What started as a loose collection of common practices shared among high-functioning software engineering teams transformed into a modern statement of engineering culture and process: DevOps. Organizations with a shared responsibility of development and operations are able to iterate faster, and as a result are more successful. DevSecOps extends that philosophy, codifying security objectives as part of the overall goal structure. DevSecOps should be thought of as the natural continuation of DevOps, rather than as a separate idea or concept. Teams that are successful in applying DevOps practices should think of DevSecOps as an evolutionary step, rather than a revolutionary one.

Many would agree that the goal was to create an environment in which business value is created by moving from code to production with a seamless and sustainable flow. With this new model came tools and methodologies that increased the pace and resulted in a bottleneck, where traditional security practices with slow feedback cycles became inhibitive of high-pace DevOps practices. As a result, security practices were often only accomplished post-production or by external teams injected into the process, thus slowing things down.

To make the difference between DevOps and DevSecOps clearer, DevSecOps extends the DevOps culture of shared responsibility to also include security practices. Activities designed to identify and ideally solve security issues are injected early in the lifecycle of application development, rather than after a product is released. This is accomplished by enabling development teams to perform many of the security tasks independently within the software development lifecycle (SDLC).

The approach helps minimize vulnerabilities that reach production, thereby reducing the cost associated with fixing security flaws. It creates scalability while also establishing a collaborative culture that brings security closer to DevOps objectives. DevSecOps aims to build security into every stage of the delivery process, from the requirement stage onwards, and establish a plan for security automation.

----

### Why are DevSecOps practices important?

Digital transformation has become an existential requirement for almost all enterprises. Such transformation includes three significant motions: more software, cloud technologies and DevOps methodologies.

More software means more of the organization’s risk becomes digital, raising the level of technical debt and therefore application security, making it increasingly challenging to secure digital assets.

Cloud means use of newer technologies that introduce different risks, change faster, are more publicly accessible — eliminating or redefining the concept of a secure perimeter. It also means many of the IT and infrastructure risks are moved to the cloud, and others are becoming purely software defined, reducing many risks while highlighting the importance of permission and access management.

Lastly, DevOps means a change to how software is developed and delivered, accelerating the cycle from writing code to delivering customer value to learning from the market and adapting. Empowered development teams ship software continuously and faster than ever, making technology and implementation decisions autonomously and without intermediaries. The traditional slow feedback loops that bog down development are not tolerated as teams increasingly prioritize being self-sufficient — you write it, you run it.

As the rest of the organization evolves, security teams are faced with greater demands and often become more of a bottleneck. Legacy application security tools and practices, designed for the slower-paced pre-cloud era, put security teams in the critical path of delivering high quality applications. These teams, understaffed due to the severe security talent shortage, become a bottleneck and fail to keep up. As a result, dev teams ship insecure applications, security teams burn out, and security becomes a naysayer, negating the acceleration the business is seeking.

To deal with these challenges, people started changing their practices and this gave birth to DevSecOps. A DevSecOps culture brings security into the DevOps fold, enabling development teams to secure what they build at their pace, while also creating greater collaboration between development and security practitioners. It allows security teams to become a supporting organization, offering expertise and tooling to increase this developer autonomy while still providing the level of oversight the business demands.

----

### 6 benefits of the DevSecOps model

![](https://snyk.io/wp-content/uploads/devsecops-benefits-1.png)

----

### 6 benefits of the DevSecOps model

* Faster delivery: The speed of software delivery is improved when security is integrated in the pipeline. Bugs are identified and fixed before deployment, allowing developers to focus on shipping features.
* Improved security posture: Security is a feature from the design phase onwards. A shared responsibility model ensures security is tightly integrated—from building, deploying, to securing production workloads.
* Reduced costs: Identifying vulnerabilities and bugs before deploying results in an exponential reduction in risk and operational cost.
* Enhancing the value of DevOps: Improving overall security posture as a culture of shared responsibility is created by the integration of security practices into DevOps.
* Improving security integration and pace: Cost and time of secure software delivery is reduced through eliminating the need to retrofit security controls post development.
* Enabling greater overall business success: Greater trust in the security of developed software and embracing new technologies enables enhanced revenue growth and expanded business offerings.

----

### DevSecOps Adoption: Integrating Security into the CI/CD Pipeline

![](https://snyk.io/wp-content/uploads/DevSecOps-Pipeline.png)

----

### DevSecOps Adoption: Integrating Security into the CI/CD Pipeline

Most modern DevOps organizations will depend on some combination of continuous integration and continuous deployment/delivery systems, in the form of a CI/CD pipeline. The pipeline is an excellent foundation from which a variety of automated security testing and validation can be performed, without requiring the manual toil of a human operator.

To integrate security objectives early in the development of an application, start before the first line of code is ever written. Security can integrate and begin effective threat modeling during the initial concept of the system, application, or individual user story. Static analysis, linters, and policy engines can be run any time a developer checks in code, ensuring that any low-hanging fruit is dealt with before the changes move further upstream.

Software composition analysis can be applied holistically to confirm that any open-source dependencies have compatible licenses and are free of vulnerabilities. A behavioral by-product of this is that developers feel a sense of ownership over the security of their applications, getting immediate feedback on the relative security of the code they’ve written.

Once the code is checked in and builds, you can start to employ security integration tests. Running the code in an isolated container sandbox allows for automated testing of things like network calls, input validation, and authorization. These tests generate fast feedback, enabling quick iteration and triage of any issues that are identified, causing minimal disruption to the overall stream. If things like unexplained network calls or unsanitized input occur, the tests fail, and the pipeline generates actionable feedback in the form of reporting and notifications to the relevant teams.

Once the deployment artifact passes the first battery of integration tests, it moves on to the next stage of integration testing. Now it will be deployed to a wider sandbox, a limited copy of the eventual production environment. At this stage, further security integration testing can be performed, albeit with a different objective. 

Now, things like correct logging and access controls can be tested. Does the application log relevant security and performance metrics correctly? Is access limited to the correct subset of individuals (or prevented entirely)? Failure again results in action items to the relevant teams.

Finally, the application makes its way to production. However, the work of DevSecOps continues in earnest. Automated patching and configuration management ensure that the production environment is always running the latest and most secure versions of software dependencies. Ideally, immutable infrastructure means that the entire environment is frequently torn down and rebuilt, constantly subjected to the battery of tests along the breadth of the pipeline.

Utilizing a DevSecOps CI/CD pipeline helps integrate security objectives at each phase, without adding burdensome bureaucracy and gatekeeping, allowing the rapid delivery of business value to be maintained.

----

### Empowering DevSecOps Culture

So how can an organization make the evolutionary climb from “DevOps” to “DevSecOps”? It’s not as simple as just handing an already busy DevOps team a set of security KPIs and calling it a day. It needs to be a collaborative, shared culture of rapid iteration.

If integrating security objectives early is the goal, it needs to be as painless as possible to do so. The burden of integrating security teams and objectives into the value stream should not fall to the developers. Adding additional steps will only lengthen the time it takes to deliver features to customers. Security should be a nimble organization, with a pragmatic approach to applying security with minimal disruption.

During the planning process, particularly as it relates to infrastructure, security engineers should be involved in discussions, empowered to push back on poor/insecure choices, but knowledgeable enough to offer alternatives. Oftentimes, overburdened security teams simply say “no,” and outsource the finding of alternatives to the DevOps teams. Again, this goes back to empowering security organizations with the right level of resources.

With security and DevOps collaborating early and often, security objectives have been tightly woven into the fabric of the infrastructure. Features and applications that are deployed to production will be the result of a comprehensive and effective collaboration between security, development, and operations. Security won’t have to go ask for extra features or auditing from development teams after the fact; they will know these were built in from day one.

If your organization has evolved to practice DevSecOps, you know that not only are you iterating quickly, delighting your customers with new features and improved functionality, but that you are delivering that experience with a level of security to match.