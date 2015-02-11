# SonarQube Runner (Sonar-Runner) container

This Docker image includes the Sonar-Runner executable, used to push Code Analysis and Coverage results to a SonarQube server.

## Pull this image

```
docker pull pierrevincent/sonar-runner
```

## Usage

By default, this image with run the sonar-runner executable inside the /data directory on the container.

### Running against your project

You project should contain a sonar-project.properties with the relevant sonar properties (such as Project Name, version etc.). Note that you can also pass these properties when running the container, e.g. -Dsonar.host.url=http://localhost:9000, this can be useful if you don't want to have user crendentials in your sonar-project.properties.