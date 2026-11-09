# Amazon Web Services (AWS) API and event test tools.  

| Category | Tool | Role | Cost | AWS fit |
|-|-|-|-|-|
|**Test framework**|xUnit|Runs unit, integration, API and Kafka tests in C#|Open source|Very good. It's just `dotnet test` in any CI. |
|**Test environment**|Testcontainers for .NET|Starts Kafka, Schema Registry and databases per test run|Open source|Good. Needs Docker, so use CodeBuild privileged mode or Docker-capable runners. |
||Confluent.Kafka client|Produce and consume in tests|Open source|Very good, including against Amazon Managed Kafka Services (MSK). |
|**Load and soak**|NBomber|C# load, soak and Kafka load tests|Commercial for organisations / [Per company.](https://nbomber.com/pricing) |Good. Runs on ECS, EC2 or CodeBuild. |
|**Resilience**|Toxiproxy|Injects network faults (including for Kafka)|Open source|Good. Runs as a container or ECS sidecar. |
||Polly (with chaos strategies)|In-app resilience policies and in-process faults|Open source|Very good. Library only, no AWS dependency. |
||Chaos Mesh|Fault injection on Kubernetes|Open source|Good on EKS. |
||AWS Fault Injection Service (FIS)|Faults on AWS resources|Pay per use|Native. / [What is FIS?](https://docs.aws.amazon.com/fis/latest/userguide/what-is.html) / [Event/data layer chaos testing](https://www.conduktor.io/glossary/chaos-engineering-for-kafka) / [FIS lambda function testing](https://aws.amazon.com/blogs/mt/introducing-aws-fault-injection-service-actions-to-inject-chaos-in-lambda-functions) / [FIS partial failure testing](https://aws.amazon.com/blogs/mt/simulating-partial-failures-with-aws-fault-injection-service)  |
|**Code quality and security**|SonarQube|Static analysis, coverage import and quality gates|Commercial for private code. [Price per instance / lines of code / year.](https://www.sonarsource.com/plans-and-pricing/sonarqube)|Very good. SaaS, so the pipeline uploads results. |
||OWASP ZAP|Runtime security scanning of the deployed API|Open source|Very good. Runs as a container in CI. |
|**Test management and Jira**|Jira Xray|Plans, cases, executions and reports in Jira|Commercial [Price per Jira user.](https://www.atlassian.com/software/jira/pricing)|Fine. SaaS, uploaded from AWS CI through its REST API. |
|**Reporting**|Allure Report|Developer and CI HTML reports|Open source|Very good. Static HTML in S3, served through CloudFront. [Check CloudFront CDN for more information.](https://aws.amazon.com/cloudfront) |
||S3 (with versioning and Object Lock)|Immutable report archive|[Per month.](https://aws.amazon.com/s3/pricing)|Native.|  

