# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

# Deployment Resource Analysis

## Virtual Machine (VM) Analysis

### Costs

Using a Virtual Machine can become expensive because the user must pay for the VM instance, storage, networking, and maintenance. Additional costs may also occur for backups, monitoring, and scaling resources manually.

### Scalability

A VM provides flexibility, but scaling must usually be handled manually. If the application traffic increases, larger VM sizes or multiple VMs would need to be configured separately using load balancers.

### Availability

Availability depends on how the VM is configured and maintained. The user is responsible for updates, monitoring, backups, and recovery processes to keep the application running properly.

### Workflow

Deploying with a VM requires more setup and maintenance. The user must configure the operating system, install dependencies, manage updates, and handle deployments manually.

---

## App Service Analysis

### Costs

Azure App Service is cost-effective for small and medium web applications because infrastructure management is handled by Azure. The Free and Basic plans are suitable for lightweight applications and reduce maintenance overhead.

### Scalability

App Service supports automatic scaling and makes it easier to increase resources when traffic grows. Scaling can be performed quickly without manually configuring servers.

### Availability

Azure App Service provides high availability and reliability through Azure-managed infrastructure. Microsoft handles server maintenance, patching, and uptime management.

### Workflow

The deployment workflow is much simpler with App Service. Applications can be deployed directly from GitHub or ZIP deployment, and Azure automatically manages the runtime environment.

---

# Deployment Choice and Justification

I selected Azure App Service for deploying the CMS application because it provides an easier deployment workflow, automatic scaling, and simplified infrastructure management. It also reduces the amount of server administration required compared to a Virtual Machine.

App Service is more suitable for this project because the CMS application is a lightweight Flask web application that does not require full operating system control. Azure manages updates, runtime configuration, and availability, which allows development to focus more on application features instead of infrastructure maintenance.

---

# Decision Change Scenario

If the application later required custom operating system configurations, advanced networking settings, or persistent local storage, then using a Virtual Machine would become a better option. A VM would provide more control over the server environment and allow additional software or services to be installed directly on the operating system.

To support those requirements, the application architecture would also need changes such as manual scaling configuration, server monitoring, operating system maintenance, backup management, and additional security configuration. This would increase infrastructure responsibility but provide greater flexibility and customization.

