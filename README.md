Devops task-3
 Provision Docker Container using Terraform

1.  Install Required Tools
   - Install Terraform and Docker locally on the system.
   - Docker is used to run containers.
   - Terraform is used to automate and manage infrastructure (in this case, Docker resources) using code.


     2. Created a Terraform file named main.tf

   - Specified the use of the Docker provider in Terraform, which enables Terraform to interact with the local Docker engine.

   - Defined a docker_image resource to pull the official nginx:latest image from Docker Hub. This image serves as the base for creating the container.

   - Defined a docker_container resource to create and run a container from the pulled Nginx image.
     - Assigned the container a name: my_nginx.
     - Configured port mapping: exposed port 80 inside the container to port 8080 on the local machine. This allows access to the containerized Nginx server via http://localhost:8080.

   - In summary:
     - Terraform initializes the Docker provider.
     - Docker pulls the required image.
     - Terraform provisions and manages the container.
     - The Nginx service becomes accessible locally through the mapped port.


3. Ran the following Terraform commands:
   - terraform init 
     (Initializes the project and downloads provider plugins)

   - terraform plan 
     (Shows what Terraform will do before applying)

   - terraform apply 
     (Actually creates the Docker container)

   - terraform state list 
     (Shows the resources Terraform is managing)

   - terraform destroy 
     (Deletes the Docker container created by Terraform)

4. Checked container was running:
   - Used "docker ps" to confirm
   - Opened browser at http://localhost:8080 to see Nginx welcome page

 We successfully used Terraform to create a Docker container.

