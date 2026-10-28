# Test tools for backend API and Kafka testing on AWS

|Category|Tool|Role|Licence|AWS fit|
|-|-|-|-|-|
|**Test framework**|xUnit|Runs unit, integration, API and Kafka tests in C#|Open source|Very good. It's just `dotnet test` in any CI|
|**Test environment**|Testcontainers for .NET|Starts Kafka, Schema Registry and databases per test run|Open source|Good. Needs Docker, so use CodeBuild privileged mode or Docker-capable runners|
||Confluent.Kafka client|Produce and consume in tests|Open source|Very good, including against Amazon MSK|
|**Load and soak**|NBomber|C# load, soak and Kafka load tests|Commercial for organisations (check)|Good. Runs on ECS, EC2 or CodeBuild|
|**Resilience**|Toxiproxy|Injects network faults (including for Kafka)|Open source|Good. Runs as a container or ECS sidecar|
||Polly (with chaos strategies)|In-app resilience policies and in-process faults|Open source|Very good. Library only, no AWS dependency|
||Chaos Mesh|Fault injection on Kubernetes|Open source|Good on EKS|
||AWS Fault Injection Service|Faults on AWS resources|Pay per use|Native. Check which MSK and ECS actions it supports|
|**Code quality and security**|SonarQube Cloud|Static analysis, coverage import and quality gates|Commercial for private code (check)|Very good. SaaS, so the pipeline just uploads results|
||OWASP ZAP|Runtime security scanning of the deployed API|Open source|Very good. Runs as a container in CI|
|**Test management and Jira**|Jira Xray|Plans, cases, executions and reports in Jira|Commercial (per Jira user)|Fine. SaaS, uploaded from AWS CI through its REST API|
|**Reporting**|Allure Report|Developer and CI HTML reports|Open source|Very good. Static HTML in S3, served through CloudFront|
||S3 (with versioning and Object Lock)|Immutable report archive|Pay per use|Native|

Licences and pricing have not been verified, so check them with each vendor before finalising.

