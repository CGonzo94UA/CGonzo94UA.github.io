---
layout: post
title: "Precision Medicine: a cloud exploration of cBioPortal"
date: 2026-04-17
categories: biomedicine cloud-computing
---

### **The challenge of genomic data**
In the era of precision medicine, the bottleneck is no longer generating data, but making sense of it. Large-scale projects like **The Cancer Genome Atlas (TCGA)** have produced petabytes of data, but for a clinical researcher, querying this information without advanced coding skills used to be nearly impossible.

### **What is cBioPortal?**
The **cBioPortal for Cancer Genomics** is an open-source platform designed to lower the barriers between complex genomic data and biomedical researchers. It provides an intuitive web interface to visualize and analyze multidimensional cancer genomics data—such as mutations, copy number alterations, and mRNA expression—alongside clinical patient outcomes.

### **Investigating the stack**
To understand how a platform of this scale operates, I used the **BuiltWith** technology profiling tool to audit the site’s infrastructure. The audit confirms that the platform relies on a cloud-native architecture primarily powered by Amazon Web Services (AWS).

You can view the full technical breakdown here: [cbioportal.org Technology Profile (builtwith.com)](https://builtwith.com/cbioportal.org).

### **Cloud infrastructure: powered by AWS**
To handle thousands of concurrent users and massive datasets, the public instance of cBioPortal is built on a cloud-native architecture using **Amazon Web Services (AWS)**. Key components of its deployment include:

* **Amazon EKS (Kubernetes):** Manages the deployment of frontend and backend containers, ensuring high availability and seamless updates.
* **Amazon EC2 & ELB:** Provides scalable computing power and distributes incoming traffic via the **Elastic Load Balancer** to prevent site crashes during high-demand periods.
* **Amazon RDS:** A managed database service (MySQL) that stores the structured genomic and clinical metadata essential for researcher queries.
* **Amazon S3:** Often used as a "Storage for the Internet" to hold static assets and large data files securely.

### **Why the Cloud matters for biomedicine**
By hosting cBioPortal in the cloud, the team at Memorial Sloan Kettering can provide a seamless experience where researchers don't have to worry about hardware limitations. Cloud hosting allows for **horizontal scaling**—meaning as more researchers use the tool, the infrastructure automatically adds more capacity to keep the analysis fast and responsive.

---

### **References**

* **BuiltWith.** (2026). *cbioportal.org Technology Profile*. Retrieved from [https://builtwith.com/cbioportal.org](https://builtwith.com/cbioportal.org)
* **Cerami, E., Gao, J., Dogrusoz, U., et al.** (2012). The cBio Cancer Genomics Portal: An Open Platform for Exploring Multidimensional Cancer Genomics Data. *Cancer Discovery*, 2(5), 401-405. [https://doi.org/10.1158/2159-8290.CD-12-0095](https://doi.org/10.1158/2159-8290.CD-12-0095)
* **Gao, J., Aksoy, B. A., Dogrusoz, U., et al.** (2013). Integrative Analysis of Complex Cancer Genomics and Clinical Profiles using the cBioPortal. *Science Signaling*, 6(269), pl1. [https://doi.org/10.1126/scisignal.2004088](https://doi.org/10.1126/scisignal.2004088)
* **cBioPortal Documentation.** (2024). *Deployment Procedure on AWS*. Retrieved from [https://docs.cbioportal.org/](https://docs.cbioportal.org/)