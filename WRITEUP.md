# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

_For **both** a VM or App Service solution for the CMS app:_

- _Analyze costs, scalability, availability, and workflow_
- _Choose the appropriate solution (VM or App Service) for deploying the app_
- _Justify your choice_

For this lightweight project which involves HTTP based service to host web application, I would prefer to go with App Service solution which is a PaaS(Platform as a Service) offering. The cloud service provider manages the underlying infrastructure such as Servers, networking, storage etc and also responsible for critical OS patches, updates and middleware components. Since the infrastrucure is being handled by cloud provider, the availability of the application will be on higher side (SLA 99.95%). Auto scaling is also possible in App service solution which depends on pricing tier we choose. Since, it can be able to configure with GitHub or other version controls, automated deployment is possible once the repository is committed with the changes.

Virtual machines on the other hand, is IaaS(Infrastructure as a Service) offering, where we have complete control over the development environment, easy to migrate legacy apps to cloud and can extend our on-premise datacenter.
Availabilty of VM is same as that of App service and hence may not be an issue. Scalability of VM is possible and increases in hardware requirement based on the requirement may be expensive.

### Assess app changes that would change your decision.

_Detail how the app and any other needs would have to change for you to change your decision in the last section._
If my app becomes considerably popular and having more concurrent users and possibilties of converting the app as a high compute application with the addition of more advanced features like uploading/playing videos etc, then with the limited scaling possibilities with the App Service solution it would not be efficient to run the app as it could potentially break the application. I would prefer to rather move to VM which would give full control on the infrastruture like CPU, RAM, storage etc, but it may become expensive in terms of hardware requirement and maintanance.
