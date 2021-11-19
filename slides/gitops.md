## GitOps

----

### What is GitOps?

GitOps is an operational framework that takes DevOps best practices used for application development such as version control, collaboration, compliance, and CI/CD tooling, and applies them to infrastructure automation. While the software development lifecycle has been automated, infrastructure has remained a largely manual process that requires specialized teams. With the demands made on today’s infrastructure, it has become increasingly crucial to implement infrastructure automation.

----

### What is GitOps?

Modern infrastructure needs to be elastic so that it can effectively manage cloud resources that are needed for continuous deployments. Modern applications are developed with speed and scale in mind. Organizations with a mature DevOps culture can deploy code to production hundreds of times per day. DevOps teams can accomplish this through development best practices such as version control, code review, and CI/CD pipelines that automate testing and deployments.

----

### What is GitOps?

GitOps is used to automate the process of provisioning infrastructure. Similar to how teams use application source code, operations teams that adopt GitOps use configuration files stored as code (infrastructure as code). GitOps configuration files generate the same infrastructure environment every time it’s deployed, just as application source code generates the same application binaries every time it’s built.

----

### How do teams put GitOps into practice?

GitOps is not a single product, plugin, or platform. GitOps workflows help teams manage IT infrastructure through processes they already use in application development. 

----

### Core components

GitOps requires three core components:
* IaC
* MR (or PR)
* CI/CD

----

### Core components

* IaC
  * GitOps uses a Git repository as the single source of truth for infrastructure definitions. Git is an open source version control system that tracks code management changes, and a Git repository is a .git folder in a project that tracks all changes made to files in a project over time. Infrastructure as code (IaC) is the practice of keeping all infrastructure configuration stored as code. The actual desired state may or may not be not stored as code (e.g., number of replicas or pods).

----

### Core components

* MRs
  * GitOps uses merge requests (MRs) as the change mechanism for all infrastructure updates. The MR is where teams can collaborate via reviews and comments and where formal approvals take place. A merge commits to your main (or trunk) branch and serves as an audit log.

----

### Core components

* CI/CD
  * GitOps automates infrastructure updates using a Git workflow with continuous integration and continuous delivery (CI/CD). When new code is merged, the CI/CD pipeline enacts the change in the environment. Any configuration drift, such as manual changes or errors, is overwritten by GitOps automation so the environment converges on the desired state defined in Git. GitLab uses CI/CD pipelines to manage and implement GitOps automation, but other forms of automation, such as definitions operators, can be used as well.

----

### GitOps challenges

With any collaborative effort, change can be tricky and GitOps is no exception. GitOps is a process change that will require discipline from all participants and a commitment to doing things in a new way. It is vital for teams to write everything down.

----

### GitOps challenges

GitOps allows for greater collaboration, but that is not necessarily something that comes naturally for some individuals or organizations. A GitOps approval process means that developers make changes to the code, create a merge request, an approver merges these changes, and the change is deployed. This sequence introduces a “change by committee” element to infrastructure, which can seem tedious and time-consuming to engineers used to making quick, manual changes.

----

### GitOps challenges

It is important for everyone on the team to record what’s going on in merge requests and issues. The temptation to edit something directly in production or change something manually is going to be difficult to suppress, but the less “cowboy engineering” there is, the better GitOps will work.

----

### What makes GitOps works?

As with any emerging technology term, GitOps isn’t strictly defined the same way by everyone across the industry. GitOps principles can be applied to all types of infrastructure automation including VMs and containers, and can be very effective for teams looking to manage Kubernetes-based infrastructure.

----

### What makes GitOps works?

While many tools and methodologies promise faster deployment and seamless management between code and infrastructure, GitOps differs by focusing on a developer-centric experience. Infrastructure management through GitOps happens in the same version control system as the application development, enabling teams to collaborate more in a central location while benefiting from Git’s built-in features.

----

### Principles of GitOps

* The entire system described declaratively.
  * With Gitops, Kubernetes is just one example of many modern cloud native tools that are “declarative” and that can be treated as code. Declarative means that configuration is guaranteed by a set of facts instead of by a set of instructions. With your application’s declarations versioned in Git, you have a single source of truth. Your apps can then be easily deployed and rolled back to and from Kubernetes. And even more importantly, when disaster strikes, your cluster’s infrastructure can also be dependably and quickly reproduced.

----

### Principles of GitOps

* The canonical desired system state versioned in Git.
  * With the declaration of your system stored in a version control system, and serving as your canonical source of truth, you have a single place from which everything is derived and driven. This trivializes rollbacks; where you can use a `Git revert` to go back to your previous application state. With Git’s excellent security guarantees, you can also use your SSH key to sign commits that enforce strong security guarantees about the authorship and provenance of your code.

----

### Principles of GitOps

* Approved changes that can be automatically applied to the system.
  * Once you have the declared state kept in Git, the next step is to allow any changes to that state to be automatically applied to your system. What's significant about this is that you don't need cluster credentials to make a change to your system. With GitOps, there is a segregated environment of which the state definition lives outside. This allows you to separate what you do and how you're going to do it.

----

### Principles of GitOps

* Software agents to ensure correctness and alert on divergence.
  * Once the state of your system is declared and kept under version control, software agents can inform you whenever reality doesn’t match your expectations. The use of agents also ensures that your entire system is self-healing. And by self-healing, we don’t just mean when nodes or pods fail—those are handled by Kubernetes—but in a broader sense, like in the case of human error. In this case, software agents act as the feedback and control loop for your operations.

----

### Key benefits of GitOps

Automated delivery pipelines roll out changes to your infrastructure when changes are made to Git. But the idea of GitOps goes further than that – GitOps uses tools to compare the actual production state of your whole application with what’s under source control and then it tells you when your cluster doesn’t match the real world.

By applying GitOps best practices, there is a ‘source of truth’ for both your infrastructure and application code, allowing development teams to increase velocity and improve system reliability.


----

### Key benefits of GitOps

The benefits of applying GitOps best practices are far reaching and provide:

* Increased Productivity
  * Continuous deployment automation with an integrated feedback control loop speeds up Mean Time to Deployment. Your team can ship 30-100 times more changes per day, increasing overall development output 2-3 times.

----

### Key benefits of GitOps

* Enhanced Developer Experience
  * Push code and not containers. Developers can use familiar tools like Git to manage updates and features to Kubernetes more rapidly without having to know the internal of Kubernetes. Newly on-boarded developers can get quickly up to speed and be productive within days instead of months.

----

### Key benefits of GitOps

* Improved Stability
  * When you use Git workflows to manage your cluster, you automatically gain a convenient audit log of all cluster changes outside of Kubernetes. An audit trail of who did what, and when to your cluster can be used to meet SOC 2 compliance and ensure stability.

----

### Key benefits of GitOps

* Higher Reliability
  * With Git’s capability to revert/rollback and fork, you gain stable and reproducible rollbacks. Because your entire system is described in Git, you also have a single source of truth from which to recover after a meltdown, reducing your meantime to recovery (MTTR) from hours to minutes.

----

### Key benefits of GitOps

* Consistency and Standardization
  * Because GitOps provides one model for making infrastructure, apps and Kubernetes add-on changes, you have consistent end-to-end workflows across your entire organization. Not only are your continuous integration and continuous deployment pipelines all driven by pull request, but your operations tasks are also fully reproducible through Git.

----

### Key benefits of GitOps

* Stronger Security Guarantees
  * Git’s strong correctness and security guarantees, backed by the strong cryptography used to track and manage changes, as well as the ability to sign changes to prove authorship and origin is key to a secure definition of the desired state of the cluster.

----

### GitOps is Continuous Delivery meets Cloud Native

Freedom to choose the tools you need

As a workflow for CI/CD pipelines GitOps has been described as the holy grail of development processes. Because there is no single tool that can do everything required in your CICD pipeline, GitOps gives you the freedom to choose the best tools for the different parts. You can select a set of tools from the open source ecosystem or from closed source or depending on your use case, you may even combine them.

----

### GitOps is Continuous Delivery meets Cloud Native

The most difficult part of creating a CICD pipeline is gluing all of the pieces together. Whatever you choose for your delivery pipeline, applying GitOps best practises with Git (or any version control) should be as an integral component of your process. Doing so will make the transition to continuous delivery easier. This is true not only from a technical point of view but also from a cultural perspective.

----

### Git enables infrastructure as code (IAC) tools

Kubernetes is just one example of many modern cloud native tools that are “declarative” and that can be treated as code. Declarative means that configuration is guaranteed by a set of facts instead of by a set of instructions, for example, “there are ten redis servers”, rather than “start ten redis servers, and tell me if it worked or not”.

----

### Git enables infrastructure as code (IAC) tools

With declarative tools, your entire set of configuration files can be version controlled in Git. By using Git as the source of truth your apps more easily deployed and rolled back to and from Kubernetes. And even more importantly, when disaster strikes, your cluster’s infrastructure can be dependably and quickly reproduced all from Git.

----

### IAC tools vs. GitOps

Infrastructure as Code tools that can provision servers on demand have existed for quite some time. These tools originated the concept of keeping infrastructure config versioned, backed up and reproducible from source control.

But now with Kubernetes being almost completely declarative, combined with the immutable container, it is possible to extend some of these concepts to managing applications and their operating system as well.

----

### IAC tools vs. GitOps

The ability to manage and compare the current state of both your infrastructure, and your applications so that you can test, deploy, rollback, rollforward with a complete audit trail all from Git is what encompasses the GitOps philosophy and its best practices. This is possible because Kubernetes is managed almost entirely through declarative config and because containers are immutable.

----

### What if my system diverges from the source of truth?

Declarative provisioning tools let you describe your desired true state in Git. But they suffer from the problem that what is “really true right now” is in the live system, and that may differ from what is described in source control.

----

### What if my system diverges from the source of truth?

* How do you know if the live system has converged to the desired state?
* Can you get notified when this differs?
* What is the “canary in the coal mine” that informs you when you’re in trouble?
* How do you trigger convergence between the cluster and source control?

----

### What if my system diverges from the source of truth?

There is prior art here.

IAC tools like Chef, Puppet and Ansible support features like “diff alerts”. These help operators to understand when action may need to be taken to “converge” the live system to the intended state (as defined by the configuration scripts). And more recently, best practice is to deploy immutable images (eg. containers) so that divergence is less likely.

----

### What if my system diverges from the source of truth?

In the “GitOps” model, we use Git to solve for divergence and convergence, aided by a set of “diff” and “sync” tools (kubediff, as well as terradiff and ansiblediff) that compare the intended state with actual state.

----

### GitOps builds on immutable infrastructure

GitOps takes full advantage of the move towards immutable infrastructure and declarative container orchestration. In order to minimize the risk of change after a deployment, whether intended or by accident via “configuration drift” it is essential that we maintain a reproducible and reliable deployment process.

----

### GitOps builds on immutable infrastructure

Our whole system’s desired state (aka “the source of truth”) is described in Git. We use containers for immutability as well as different cloud native tools like Terraform and Ansible to automate and manage our configuration. These tools together with containers and declarative nature of Kubernetes provide what we need for a complete recovery in the case of an entire meltdown.

----

### Works with IAC tools

When you apply GitOps principles to “everything”, including machine configuration, applications and services in addition to alerting rules and dashboards, all are kept under source control.

----

### Works with IAC tools

Access to the running system should not be required except via Git. Any group of changes may be applied atomically, and diffed accordingly. The Git record is then not just an audit log but also a transaction log that you can use to roll back and forth to any snapshot.

----

### Kubernetes controller implemented with the operator pattern

GitOps implements a custom controller to listen for and synchronize deployments to your Kubernetes cluster. The controller is implemented using the operator pattern which is significant on two levels; first, it is more secure, and; secondly, it automates complex error prone tasks like having to manually update YAML manifests.

----

### Kubernetes controller implemented with the operator pattern

By using the operator pattern, an agent acts on behalf of the cluster to listen to events relating to custom resource changes, so that they can be applied. The agent is responsible for synchronizing what’s in Git with what’s running in the cluster and provides a simple way for your team to achieve continuous deployment.

----

### Push Pipelines

Most CI/CD tools available today use a push-based model. A push-based pipeline means that code starts with the CI system and may continue its path through a series of encoded scripts or uses ‘kubectl’ by hand to push any changes to the Kubernetes cluster.

----

### Push Pipelines

The reason you don’t want to use your CI system as the deployment impetus or do it manually on the command line is because of the potential to expose credentials outside of your cluster. While it is possible to secure both your CI/CD scripts and the command line, you are working outside the trust domain of your cluster. This is generally not good practice and is why CI systems can be known as attack vectors for production.

----

### Pull Pipeline

GitOps uses a pull strategy that consists of two key components: a “Deployment Automator” that watches the image registry and a “Deployment Synchronizer” that sits in the cluster to maintain its state.

----

### Pull Pipeline

At the centre of our pull pipeline pattern is a single source of truth for manifests (or a config repo). Developers push their updated code to the code base repository; where the change is picked up by the CI tool and ultimately builds a Docker image. The ‘Deployment Automator’ notices the image, pulls the new image from the repository and then updates its YAML in the config repo. The Deployment Synchronizer, then detects that the cluster is out of date, and it pulls the changed manifests from the config repo and deploys the new image to the cluster.

----

### Pipelines

![](https://images.contentstack.io/v3/assets/blt300387d93dabf50e/blt949977aec622d0b5/5ff7877db80b0a1a68fa2d3f/cicd2.png)

----

### Pipelines

![](https://images.contentstack.io/v3/assets/blt300387d93dabf50e/blt31fc28ca69fa30a8/5a5e940703361d7a0b2936a5/gitops_cd_pipeline.png)

----

### Observability as a deployment catalyst

With Kubernetes, GitOps can manage infrastructure and app deployments through pull-requests. But how do GitOps workflows and observability work together? 

----

### Observability as a deployment catalyst

By combining GitOps workflows with real-time observability, your development team can make crucial decisions before they deploy any new features. Because about to be released services can be observed in real-time within the running cluster before you release, it means that you can deploy with confidence and deliver better quality features more quickly. 

----

### Observability as a deployment catalyst

Observability can be seen as one of the principal drivers of the Continuous Delivery cycle for Kubernetes since it describes the actual running state of the system at any given time. The running system is observed in order to understand and control it. New features and fixes are pushed to git and trigger the deployment pipeline, and when ready to be released can be observed in real-time against the running cluster. At this point, the developer may return to the beginning of the pipeline based on this feedback or deploy and release the image to the production cluster.

----

### Observability as a deployment catalyst

GitOps is a release oriented model of both operations and features. How quickly you deliver new features to your customers, depends in part on how fast your team can go round the stages in this cycle.

----

### Observability

![](https://images.contentstack.io/v3/assets/blt300387d93dabf50e/blt9007410e82bb7c90/5b2bef8ab54f861f064be969/rooda2.png)

----

### Faster development

By adopting GitOps best practices developers use familiar tools like Git to manage updates and features to Kubernetes more rapidly. By continuously pushing feature updates, businesses are more agile, can respond more quickly to customer demands, and are more competitive in the marketplace.

----

### Better Ops

With GitOps you have a complete end to end pipeline. Not only are your continuous integrations and continuous deployment pipelines all driven by pull request, but your operations tasks are also fully reproducible through Git.

----

### Stronger security guarantees

Git’s strong correctness and security guarantees, backed by the strong cryptography used to track and manage changes, as well as the ability to sign changes to prove authorship and origin is key to a correct and secure definition of desired state of the cluster. If a security breach does occur, the immutable and auditable source of truth can be used to recreate a new system independently of the compromised one, reducing downtime and allowing much better incident response.

----

### Stronger security guarantees

Separation of responsibility between packaging software and releasing it to a production environment also embodies the security principle of least privilege, reducing the impact of compromise and providing a smaller attack surface.

----

### Easier compliance and auditing

Since changes are tracked and logged in a secure manner, compliance and auditing are made trivial. The use of comparison tools like kubediff, terradiff and ansiblediff also allow you to compare a trusted definition of the state of the cluster with the actual running cluster, ensuring that the tracked and auditable changes match reality.