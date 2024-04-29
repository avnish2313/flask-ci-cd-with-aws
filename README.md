# Flask Web Application

This is a simple Flask web application project for demonstrating a CI/CD pipeline using GitHub Actions and AWS services.

## Overview

The project includes a basic Flask web application (`app.py`) and unit tests (`test.py`) to ensure the application functions as expected. The CI/CD pipeline automates the build, test, and deployment processes, integrating GitHub Actions for initial CI and AWS services (CodeBuild, CodePipeline, CodeDeploy) for the complete CI/CD workflow.

## Repository Structure

project-repository/

│

├── app.py

├── test.py

├── requirements.txt

│
- `app.py`: Main Flask application file.
- `test.py`: Unit tests for the application.
- `.github/workflows/main.yml`: GitHub Actions workflow for initial CI.
- `buildspec.yml`: AWS CodeBuild configuration.
- `appspec.yml`: AWS CodeDeploy configuration.
- `requirements.txt`: Python dependencies for the application.

## Getting Started

To run the application locally:

1. Install Python (if not already installed).
2. Clone this repository: `git clone https://github.com/avnish2313/flask-ci-cd-with-aws.git`
3. Navigate to the project directory: `cd project-repository`
4. Install dependencies: `pip install -r requirements.txt`
5. Run the application: `python app.py`
6. Open your web browser and go to `http://localhost:5000` to view the application.

## CI/CD Pipeline

The CI/CD pipeline automates the following processes:

- Continuous Integration (CI) using GitHub Actions:
  - GitHub Actions workflow (`main.yml`) triggers on every push to the `main` branch.
  - Builds the application, runs tests, and notifies about the build status.

- Continuous Deployment (CD) using AWS services:
  - AWS CodeBuild builds the application and produces artifacts.
  - AWS CodePipeline orchestrates the CI/CD workflow, triggering builds and deployments.
  - AWS CodeDeploy deploys the application to staging and production environments.
