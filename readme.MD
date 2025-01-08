In AWS, you can scan container images for vulnerabilities using Amazon Elastic Container Registry (ECR) integrated with Amazon Inspector, or leverage third-party security tools. Here's how to do it:
# Step 1: Enable Image Scanning on ECR
* First, ensure that you have image scanning enabled for your repositories in Amazon ECR. You can do this when you push images to ECR, or by configuring your repository to perform scanning automatically.
* Navigate to the ECR console, select the repository, and enable Image scanning on push.

![50](https://github.com/user-attachments/assets/2a2ea57b-7b61-48a2-bb28-c1be93afcebf)

# Step 2: Scan the Container Image
oYou can also manually trigger a scan from the AWS Management Console by selecting the image in your ECR repository and choosing Scan.

![51](https://github.com/user-attachments/assets/5189d179-f964-4ffd-b98c-dcf2871d65b6)

* Click on the scan option after opening an image.

![52](https://github.com/user-attachments/assets/eb93334b-6334-4bdb-86cb-9594b8ab3abe)

# Step 3: View Vulnerability Findings
* After the scan completes, you can view the findings directly in the Amazon Inspector section of the AWS console.
oAmazon Inspector provides a comprehensive report detailing the vulnerabilities found, categorized by severity (e.g., critical, high, medium, low).

# Step 4: Mitigation
* Patch vulnerabilities: Update the affected container image by replacing vulnerable components with patched versions. Rebuild the container and push it to the ECR repository.
* Use minimal base images: If possible, use minimal container base images (like Alpine or distroless images) to reduce the attack surface.

* Implement image scanning during the CI/CD pipeline: Integrate vulnerability scanning into your continuous integration and deployment (CI/CD) pipeline to catch vulnerabilities early.
Vulnerabilities found after scan.

![53](https://github.com/user-attachments/assets/0fab7670-a06c-48df-9b79-24303b3306b4)

![54](https://github.com/user-attachments/assets/0b12c2b1-8242-4284-8341-d04a71248741)
