
# Day 16 — CI/CD Fundamentals, Deployment Strategies, and DevOps Principles

**Training Date:** 22 July 2026

## 1. Overview

Day 16 focused on understanding the fundamentals of Continuous Integration and Continuous Delivery/Deployment (CI/CD), an important part of modern DevOps practices. The session covered the major stages of a CI/CD pipeline, the challenges associated with manual software deployment, and the purpose of maintaining separate development, staging, and production environments.

Different deployment strategies, including Blue-Green Deployment, Canary Deployment, and Rolling Deployment, were also explored. In addition, the session introduced the DevOps lifecycle and the CAMS principles: Culture, Automation, Measurement, and Sharing.

These concepts help explain how development teams can deliver software more efficiently, reduce deployment risks, improve collaboration, and maintain consistent software delivery workflows.

## 2. Topics Covered

### 2.1 Introduction to CI/CD

CI/CD refers to practices that automate and improve the process of integrating code changes, validating software, and delivering applications to users.

CI/CD commonly stands for:

- **Continuous Integration (CI):** The practice of frequently integrating code changes into a shared repository and validating them through automated builds and tests.
- **Continuous Delivery (CD):** The practice of keeping software in a deployable state so that it can be released reliably when required.
- **Continuous Deployment (CD):** An approach in which changes that successfully pass the required automated checks are automatically released to production.

Continuous Delivery and Continuous Deployment are related but different. Continuous Delivery generally retains a release approval step, whereas Continuous Deployment automates the production release process as well.

#### Why CI/CD Is Important

CI/CD helps development teams:

- Detect problems earlier in the development process.
- Reduce repetitive manual work.
- Deliver software updates more frequently.
- Improve consistency in builds and deployments.
- Reduce the risk of errors caused by manual procedures.
- Make software changes easier to test and validate.

### 2.2 Understanding a CI/CD Pipeline

A **CI/CD pipeline** is a sequence of automated or partially automated stages used to move software changes from development toward release and deployment.

The session covered four main stages: Development, Build, Testing, and Deployment/Release.

#### Stage 1: Development

Development is the stage where developers write and modify application code.

Typical activities include:

- Developing new features.
- Fixing bugs.
- Updating existing functionality.
- Saving and managing changes through version control systems such as Git.
- Sharing code changes through a repository such as GitHub.

The development stage produces code changes that can be integrated and validated.

#### Stage 2: Build

The build stage prepares the application for testing or deployment.

Depending on the technology used, this stage may involve:

- Compiling source code.
- Resolving or installing dependencies.
- Packaging application files.
- Creating executable artifacts.
- Building a Docker image when containerization is used.

A successful build indicates that the application has passed the build process, although it does not necessarily mean that the application is free of defects.

#### Stage 3: Testing

The testing stage checks whether the application behaves as expected and meets defined requirements.

Testing may include:

- **Unit Testing:** Testing individual functions or components.
- **Integration Testing:** Checking whether different components work together correctly.
- **Functional Testing:** Verifying that application features behave as intended.
- **Security Checks:** Identifying certain security weaknesses through automated tools.
- **Quality Checks:** Validating code against defined standards.

Automated testing helps identify defects before an application reaches its users.

#### Stage 4: Deployment and Release

The deployment and release stage makes the application available in the intended environment.

Activities may include:

- Deploying application artifacts to a server or cloud platform.
- Updating a running application.
- Configuring the application environment.
- Verifying that the deployed application is working correctly.
- Releasing the application to its intended users.

Deployment may be performed manually after automated validation in a Continuous Delivery workflow, or automatically in a Continuous Deployment workflow.

### 2.3 Challenges of Manual Software Deployment

Manual deployment involves carrying out deployment activities through individual actions rather than relying on a consistently automated process.

Although manual procedures may be manageable for small applications, they can become difficult to maintain as applications and infrastructure grow.

#### Common Challenges

**1. Human Errors**

Manually entering commands, modifying configuration files, or copying application files can lead to mistakes.

**2. Inconsistent Environments**

Different configurations between development, staging, and production can cause applications to behave differently after deployment.

**3. Time Consumption**

Repeated manual tasks require time and effort, especially when deploying frequently or managing multiple environments.

**4. Difficult Rollbacks**

If a deployment introduces a problem, restoring the previous working version may require additional manual steps.

**5. Limited Repeatability**

When deployment depends on individual knowledge or undocumented procedures, repeating the same process consistently becomes difficult.

**6. Reduced Visibility**

Without appropriate logging, monitoring, and deployment records, it may be difficult to identify which changes were deployed and when a failure occurred.

#### How Automation Helps

CI/CD pipelines can automate repeatable tasks such as building applications, running tests, packaging artifacts, and deploying validated versions.

Automation does not eliminate every possible failure, but it can reduce avoidable manual errors and make the delivery process more consistent and traceable.

### 2.4 Development, Staging, and Production Environments

Software is commonly developed and tested in separate environments before being released to actual users.

An **environment** is a configured setup in which an application runs. Different environments support different stages of software development and release.

#### A. Development Environment

The development environment is used by developers to write code, implement features, and test changes during development.

Characteristics:

- Frequent code changes are expected.
- Developers can experiment with new functionality.
- Features and bug fixes are developed and tested.
- The environment may contain incomplete or experimental changes.

#### B. Staging Environment

The staging environment is used to validate an application before production release.

It is generally configured to resemble production as closely as practical.

Characteristics:

- Candidate releases can be tested before going live.
- Integration and acceptance checks can be performed.
- Configuration and deployment procedures can be verified.
- Potential release issues can be identified before users are affected.

#### C. Production Environment

The production environment is where the live application runs and serves its intended users.

Characteristics:

- Reliability and availability are important.
- Changes should follow appropriate validation and release procedures.
- Monitoring and incident response help maintain service quality.
- Security and access controls must be carefully managed.

#### Comparison of Environments

| Basis of Difference | Development | Staging | Production |
|---|---|---|---|
| Purpose | The development environment is used to write code and implement new features. | The staging environment is used to validate release candidates before production deployment. | The production environment runs the application for its actual users. |
| Code Changes | Code changes occur frequently as developers build and modify features. | Changes are introduced mainly to validate a candidate release and its configuration. | Changes are controlled carefully to minimize disruption to live users. |
| Testing | Developers perform initial checks and tests while building features. | More complete release validation and acceptance testing can be performed. | Monitoring and production checks help identify issues affecting live operation. |
| Stability | The environment may contain incomplete or experimental changes. | The environment should be sufficiently stable to support release validation. | The environment should prioritize stability, reliability, and availability. |
| Users | It is primarily used by developers and the development team. | It is primarily used by testers, developers, and release stakeholders. | It serves the application's intended users or customers. |

### 2.5 Deployment Strategies

A deployment strategy defines how a new application version is introduced into an environment.

The choice of strategy affects downtime, risk, resource requirements, and the ability to recover from deployment problems.

Three strategies were explored: Blue-Green Deployment, Canary Deployment, and Rolling Deployment.

#### A. Blue-Green Deployment

Blue-Green Deployment uses two production-like environments:

- **Blue Environment:** The currently active version of the application.
- **Green Environment:** The new version being prepared for release, or vice versa.

The new version is deployed and tested in the inactive environment. Once it is ready, traffic is switched from the active environment to the new one.

**Example workflow:**

1. The existing application runs in the Blue environment.
2. The new version is deployed to the Green environment.
3. The Green environment is tested.
4. Traffic is switched to the Green environment.
5. If a problem occurs, traffic may be switched back to Blue, provided the previous environment remains available and compatible with the current system state.

**Advantages:**

- Can reduce downtime during releases.
- Allows the new version to be tested before traffic is switched.
- Can simplify rollback by switching traffic back to the previous environment.

**Limitations:**

- Requires additional infrastructure capacity for two environments.
- Database changes and persistent data compatibility can make rollback more complicated.

#### B. Canary Deployment

Canary Deployment introduces a new version to a small portion of users or traffic before making it available to everyone.

This allows teams to observe the new version under real operating conditions while limiting the initial impact of potential problems.

**Example workflow:**

1. The current version continues serving most users.
2. The new version is deployed to a small subset of traffic.
3. The team monitors errors, performance, and other relevant metrics.
4. If results are satisfactory, the percentage of traffic using the new version is gradually increased.
5. If serious problems occur, traffic can be redirected away from the new version.

**Advantages:**

- Limits the initial exposure to a new release.
- Provides useful feedback from real usage.
- Allows problems to be detected before a full rollout.

**Limitations:**

- Requires suitable traffic routing and monitoring.
- Running multiple versions simultaneously can increase operational complexity.

#### C. Rolling Deployment

Rolling Deployment gradually replaces existing application instances with new instances.

Instead of updating every instance at once, the deployment process updates a portion of the instances at a time.

**Example workflow:**

1. The application is running on multiple instances.
2. A subset of instances is updated to the new version.
3. The updated instances are checked for health and correct operation.
4. Additional instances are updated in subsequent batches.
5. The rollout continues until all intended instances run the new version.

**Advantages:**

- Avoids replacing all instances simultaneously.
- Can maintain application availability when sufficient healthy capacity remains.
- Allows the release to progress in manageable stages.

**Limitations:**

- Requires careful management of capacity and instance health.
- Different application versions may run simultaneously during the rollout.
- Rollback can be more involved than switching traffic between two complete environments.

#### Comparison of Deployment Strategies

| Basis of Difference | Blue-Green Deployment | Canary Deployment | Rolling Deployment |
|---|---|---|---|
| Basic Approach | Blue-Green Deployment switches traffic between two production-like environments. | Canary Deployment initially sends a small portion of traffic to the new version. | Rolling Deployment updates existing application instances in batches. |
| Release Exposure | The new version receives the main traffic after the switch. | The new version initially serves a limited portion of traffic. | The new version gradually replaces the old version across instances. |
| Infrastructure | It generally requires capacity for two production-like environments. | It requires the ability to route traffic between versions and monitor results. | It updates existing instances progressively and requires sufficient healthy capacity. |
| Rollback | Traffic may be switched back to the previous environment if it remains usable. | Traffic can be redirected away from the new version when problems are detected. | Updated instances may need to be rolled back or redeployed to the previous version. |
| Main Benefit | It can make traffic switching and application rollback straightforward. | It limits initial exposure and supports gradual validation with real traffic. | It allows updates to be introduced gradually without replacing every instance at once. |

### 2.6 Introduction to DevOps

DevOps is a set of practices, cultural principles, and tools that brings software development and IT operations closer together.

Traditionally, development teams focus on building software, while operations teams focus on running and maintaining it. DevOps encourages these teams to collaborate throughout the software lifecycle.

The goal is to improve the speed, quality, reliability, and consistency of software delivery.

#### Benefits of DevOps

- **Faster Delivery:** Automation and improved collaboration can shorten release cycles.
- **Better Collaboration:** Development and operations teams share responsibility for software delivery.
- **Improved Quality:** Automated testing helps identify defects earlier.
- **Greater Consistency:** Repeatable processes reduce unnecessary variation between deployments.
- **Faster Feedback:** Monitoring and testing provide information that teams can use to improve software.
- **Continuous Improvement:** Teams use feedback and measurements to refine their practices.

### 2.7 Understanding the DevOps Lifecycle

The DevOps lifecycle represents the ongoing activities involved in planning, developing, delivering, operating, and improving software.

The exact stages and terminology may vary between organizations, but a commonly used model includes the following activities:

#### 1. Plan

Teams define requirements, identify tasks, and plan the features or improvements to be delivered.

#### 2. Develop

Developers write and modify source code while using version control to track changes.

#### 3. Build

Source code and dependencies are processed to create a usable software artifact or application package.

#### 4. Test

The application is checked to identify defects and verify that it meets expected requirements.

#### 5. Release

A validated version is prepared and approved for delivery.

#### 6. Deploy

The application is installed or released into the intended environment.

#### 7. Operate

The application and its supporting infrastructure are managed to maintain reliable service.

#### 8. Monitor

Application performance, errors, availability, and other relevant metrics are observed. The resulting feedback helps teams plan further improvements.

The lifecycle is continuous because feedback from operation and monitoring informs future development and planning.

### 2.8 CAMS Principles of DevOps

CAMS stands for **Culture, Automation, Measurement, and Sharing**. These principles describe important ideas that support the adoption of DevOps practices.

#### C — Culture

Culture focuses on collaboration, communication, and shared responsibility between development, operations, and other relevant teams.

Rather than working in isolated groups, teams coordinate their efforts to improve the entire software delivery process.

Examples include:

- Sharing responsibility for application quality.
- Communicating across teams.
- Learning from failures instead of focusing only on blame.
- Encouraging cooperation and continuous improvement.

#### A — Automation

Automation involves using tools and scripts to perform repetitive tasks with less manual intervention.

Examples include:

- Automated builds.
- Automated testing.
- Infrastructure provisioning.
- Application deployment.
- Repetitive operational tasks.

Automation can improve consistency, reduce manual effort, and make software delivery more repeatable.

#### M — Measurement

Measurement involves collecting and analyzing data about software development, delivery, and operation.

Useful measurements may include:

- Deployment frequency.
- Time required to deliver changes.
- Build and test failure rates.
- Application availability.
- Error rates and recovery time.

Measurement helps teams identify bottlenecks, evaluate improvements, and make informed decisions.

#### S — Sharing

Sharing focuses on distributing knowledge, feedback, and responsibility across teams.

Examples include:

- Documenting processes and solutions.
- Sharing lessons learned from incidents.
- Reviewing code collaboratively.
- Communicating deployment outcomes.
- Making useful information accessible to relevant team members.

Sharing reduces knowledge silos and helps teams learn from one another.

## 3. Key Learnings

By the end of the session, the following concepts were understood:

- Learned the fundamentals of Continuous Integration and Continuous Delivery/Deployment.
- Understood the Development, Build, Testing, and Deployment/Release stages of a CI/CD pipeline.
- Identified common challenges associated with manual software deployment.
- Understood the roles of Development, Staging, and Production environments.
- Compared Blue-Green, Canary, and Rolling Deployment strategies.
- Learned the fundamentals of DevOps and its role in software delivery.
- Explored the major stages of the DevOps lifecycle.
- Understood the CAMS principles: Culture, Automation, Measurement, and Sharing.

## 4. Learning Outcome

Day 16 provided a foundational understanding of CI/CD, deployment environments, software release strategies, and DevOps principles.

The session demonstrated how automation can reduce repetitive deployment work, how separate environments support safer software validation, and how deployment strategies help teams introduce new application versions with controlled risk.

The DevOps lifecycle and CAMS principles highlighted that successful DevOps adoption involves more than tools alone. It also depends on collaboration, automation, measurement, knowledge sharing, and continuous improvement.

---

[⬅️ Back to Training Diary](../README.md)
