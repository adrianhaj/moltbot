# moltbot Docker Image

This repository contains the GitHub Actions workflow to build and publish the [moltbot](https://github.com/openclaw/openclaw) Docker image to Docker Hub.

## Workflow

The GitHub Actions workflow automatically builds and pushes the Docker image when:
- Code is pushed to the `main` or `master` branch
- Manually triggered via workflow dispatch

## Image Details

- **Docker Hub**: `heimdall777/openclaw`
- **Source**: [moltbot/clawdbot](https://github.com/openclaw/openclaw)
- **Base Image**: `node:22-bookworm`

## Tags

Images are tagged with the moltbot version from `package.json`:
- `heimdall777/openclaw:<version>` (e.g., `heimdall777/openclaw:2026.1.23`)
- `heimdall777/openclaw:latest` (always points to the most recent version)

## Usage

```bash
docker pull heimdall777/openclaw:latest
docker run heimdall777/openclaw:latest
```

## Secrets

To enable automatic builds, configure these repository secrets:
- `DOCKER_USERNAME`: Your Docker Hub username
- `DOCKER_PASSWORD`: Your Docker Hub password or access token
