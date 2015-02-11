# SonarQube Runner (Sonar-Runner) container

This Docker image includes the Sonar-Runner executable, used to push Code Analysis and Coverage results to a SonarQube server. (see http://docs.sonarqube.org/display/SONAR/Analyzing+with+SonarQube+Runner)

## Pull this image

```
docker pull pierrevincent/sonar-runner
```

## Usage

By default, this image with run the sonar-runner executable inside the /data directory on the container.

### Running against your project

You can make your project directory available to the container by sharing a volume when starting the container, using -v.
```
docker run --rm -v /path/to/your/project:/data pierrevincent/sonar-runner
```

You project should contain a sonar-project.properties with the relevant sonar properties (such as Project Key, Name, Version etc.). Note that you can also pass these properties when running the container, e.g. -Dsonar.host.url=http://localhost:9000, this can be useful if you don't want to have user crendentials in your sonar-project.properties.