# Jenkins CI/CD Pipeline for Java Maven Projects  

This repository contains a **Jenkinsfile** that automates the CI/CD process for a Java-based project using **Maven, SonarQube, and Nexus Repository**.  


## 📢 Note  
This pipeline is designed for environments where **Jenkins, SonarQube, Nexus, and Slack** are pre-configured. Without these services, the pipeline **will not function correctly**.    


## 📌 Project Overview  
The **Jenkinsfile** defines a multi-stage pipeline that performs the following tasks:  
- **Fetch Code** → Clones the repository from GitHub.  
- **Build** → Uses Maven to compile and package the application.  
- **Run Unit Tests** → Executes `mvn test` to validate code.  
- **Code Quality Analysis** → Runs Checkstyle and SonarQube for static code analysis.  
- **Quality Gate Check** → Ensures code meets SonarQube quality standards.  
- **Artifact Upload** → Deploys the `.war` file to Nexus Repository.  
- **Slack Notifications** → Sends build status updates to a Slack channel.  

## 🛠️ Required Configurations  
To successfully execute this pipeline, the following services must be configured within Jenkins:  
- **SonarQube** for code quality analysis.  
- **Nexus Repository** for artifact storage.  
- **Slack Webhook** for build notifications.  
