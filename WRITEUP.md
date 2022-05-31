# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

_For **both** a VM or App Service solution for the CMS app:_

- _Analyze costs, scalability, availability, and workflow_
- _Choose the appropriate solution (VM or App Service) for deploying the app_
- _Justify your choice_

For this lightweight project which involves HTTP based service to host web application, I would prefer to go with App Service solution which is a PaaS(Platform as a Service) offering. The cloud service provider manages the underlying infrastructure such as Servers, networking, storage etc and also responsible for critical OS patches, updates and middleware components.

Virtual machines on the other hand, is IaaS(Infrastructure as a Service) offering, where we have complete control over the development environment, easy to migrate legacy apps to cloud and can extend our on-premise datacenter.

Availability:
In App Service, since the infrastrucure is being handled by cloud provider, the availability of the application will be on higher side, which is same as that in VM as well with SLA of 99.95% of the time.

Workflow:
Deployment process is fairely easy in App service when compared with VM, because in App service we can be able to configure the application with GitHub or other version controls, CI/CD pipeline configuration is possible to have automated deployment when the configured repo is committed with changes.

Cost:
When we compare Basic tier in App service (1 Core, 1.75GB, 10 GB Storage) with Basic tier in VM (1 vCPU, 1.75GB RAM, 40GB Storage) and with Linux based machine, the approx cost is $13.14 and $22.63 respectively. For this light weight application, it would be suffice to choose App service solution with Basic tier plan or Free tier plan when compared with VM.

Scalability:
Auto scale up and scale down is possible in both VM and App service solution. They also supports built in Auto scale features, integrated load balancer. But App service can be scaled upto the extend of 30 instances, 100 with App service environment whereas VM supports 1000 nodes per scale set for platform images and 600 nodes per scale set for custom images. Again for this lightweight CMS application, basic scaling with App service is suffice.

Decision: Based on the above consideration, I would prefer to choose App Service Solution for this CMS application.

### Assess app changes that would change your decision.

_Detail how the app and any other needs would have to change for you to change your decision in the last section._
If my app becomes considerably popular and having more concurrent users and possibilties of converting the app as a high compute application with the addition of more advanced features like uploading/playing videos etc, then with the limited scaling possibilities with the App Service solution it would not be efficient to run the app as it could potentially break the application. I would prefer to rather move to VM which would give full control on the infrastruture like CPU, RAM, storage etc, but it may become expensive in terms of hardware requirement and maintanance.
