# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 
## Additional Deployment and Containerization Notes

For this project, I selected Azure App Service because it provides an easier deployment workflow, automatic scaling support, and simplified management compared to maintaining a Virtual Machine manually. It is more suitable for small and medium web applications like this CMS project.

If the application grows larger in the future, containerization using Docker could also be considered. Docker would help package the Flask application along with all dependencies into a single container, making deployment more consistent across different environments.

### Docker Compose and Persistent Storage

Docker Compose can be useful when managing multiple services together such as:

* Flask application
* SQL database
* Storage or caching services

Using Docker volumes would also help preserve uploaded image data and database-related files even after restarting containers.

### Logging and Monitoring

Application logging is important for monitoring login attempts, deployment activity, and runtime errors. Azure Log Stream was used in this project to observe application behavior during deployment and testing.

Health checks can also be added in future improvements to verify:

* Application availability
* Database connection status
* Blob storage accessibility

These improvements would make the deployment more reliable, maintainable, and production-ready.
