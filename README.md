# CD DevSecOps Project

This project demonstrates a Continuous Delivery pipeline with DevSecOps practices using GitHub Actions, Docker, Flask, Trivy, and SonarQube.

## Structure

```
/cd-devsecops-project
├── .github/workflows/
│   └── cd-pipeline.yml
├── app/
│   ├── main.py
│   ├── requirements.txt
│   └── Dockerfile
├── sonar-project.properties
├── README.md
```

## Run Locally

```bash
cd app
docker build -t devsecops-app .
docker run -p 5000:5000 devsecops-app
```
