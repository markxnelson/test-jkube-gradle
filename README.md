# Demo Application

A Spring Boot application with Kubernetes deployment capabilities using Eclipse JKube.

## Gradle Commands

### Build JAR
Build the Spring Boot JAR file:
```bash
./gradlew bootJar
```

### Build Container Image
Build the Docker container image:
```bash
./gradlew k8sBuild
```

Alternatively, build an OCI image using Spring Boot's buildpacks:
```bash
./gradlew bootBuildImage
```

### Push Container Image
Push the built container image to a registry:
```bash
./gradlew k8sPush
```

### Generate Kubernetes Manifests
Generate Kubernetes resource manifests:
```bash
./gradlew k8sResource
```

### Push Manifests (Deploy)
Apply the generated manifests to Kubernetes cluster:
```bash
./gradlew k8sApply
```

### Complete Build and Deploy Pipeline
To build, push image, generate manifests, and deploy in sequence:
```bash
./gradlew k8sBuild k8sPush k8sResource k8sApply
```

## Additional Commands

### View Configuration
View the current JKube configuration:
```bash
./gradlew k8sConfigView
```

### Undeploy
Remove the application from Kubernetes:
```bash
./gradlew k8sUndeploy
```

### View Logs
Tail logs from the deployed application:
```bash
./gradlew k8sLog
```