# CI/CD Static Web Page Deployment with GitHub Actions

## 📌 Project Overview
This repository contains a simple static web application built as an educational assignment for the **Advanced Software Engineering** course. The primary objective of this task is to demonstrate automated build and deployment processes (CI/CD pipeline) using **GitHub Actions** to host a static website on **GitHub Pages**.

---

## 👥 Team Members
The static webpage (`index.html`) displays the project team members along with their corresponding Student IDs:

| Member Name | Student ID |
| :--- | :--- |
| **Nour Ahmed Mohamed Sayed Osman** | *20242376* |
| **Dalia Sami Abdul-Aziz** | *20242116* |
| **Salma Mohsen Sayed** | *20240237* |

*(Note: Please update the placeholder names and IDs above with your team details).*

---

## ⚙️ Technical Details & Concepts

This task covers key concepts in software delivery and automation:

* **Static HTML Page (`index.html`)**: A simple, responsive web page displaying team details.
* **GitHub Repository**: Centralized version control repository hosting the project code and workflow configuration.
* **Continuous Integration & Continuous Deployment (CI/CD)**: An automated workflow designed to build, verify, and deploy the application automatically whenever new code is pushed to the repository.
* **GitHub Actions**: The automation platform used to execute the CI/CD pipeline steps.
* **YAML Workflow (`.github/workflows/deploy.yml`)**: A configuration file defining the instructions, triggers, permissions, and execution steps for the GitHub Actions runner.
* **GitHub Pages**: The cloud hosting service that serves the deployed HTML page to the public.

---

## 🚀 Workflow Architecture (`deploy.yml`)

The automated deployment pipeline performs the following sequential steps on every `push` to the `main` branch:

1. **Trigger (`on: push`)**: Listens for any code updates pushed to the `main` branch.
2. **Environment Setup**: Provisions an `ubuntu-latest` runner virtual machine.
3. **Repository Checkout (`actions/checkout@v4`)**: Clones the source code from the repository into the runner environment.
4. **Pages Setup (`actions/configure-pages@v5`)**: Configures GitHub Pages settings for automated deployment.
5. **Artifact Upload (`actions/upload-pages-artifact@v3`)**: Packages the static web files (including `index.html`) from the root directory into a deployment artifact.
6. **Deployment (`actions/deploy-pages@v4`)**: Publishes the uploaded artifact to GitHub Pages and generates the live website URL.

---

## 🌐 Live Demo
You can view the live deployed application here:  
👉 **[Live Project Link](https://nour-ahmed7.github.io/CI-CD-GitHub-Actions/)**
