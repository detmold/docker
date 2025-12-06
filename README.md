# angular-nest-docker-ci-demo

Minimal prototype repository that demonstrates building two services (frontend + backend),
Dockerizing them and a GitHub Actions workflow that builds and pushes Docker images to DockerHub.

Structure:
- frontend/         (simple static site simulating Angular build)
- backend/          (simple Node API simulating NestJS output)
- .github/workflows/deploy.yml

Instructions:
1. Unzip and `git init` / create repo on GitHub.
2. Add GitHub secrets in the repo settings:
   - DOCKERHUB_USERNAME
   - DOCKERHUB_TOKEN
3. Commit and push to `main`. The workflow will run on push to main and push images:
   - ${DOCKERHUB_USERNAME}/frontend-app:latest
   - ${DOCKERHUB_USERNAME}/backend-api:latest

Notes:
- This repo uses minimal JS scripts for "build" so Docker builds work without Angular/Nest CLI.
- You can replace the frontend/backend with real Angular/Nest projects later; Dockerfiles and workflow are compatible ttt.
