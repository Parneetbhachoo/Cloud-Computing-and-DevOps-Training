
# Day 17 — Jenkins, CI/CD Automation, and Jenkins Pipelines

**Training Date:** 23 July 2026

## 1. Overview

Day 17 focused on Jenkins, an automation server widely used in DevOps to automate software development workflows. The session explored how Jenkins supports Continuous Integration and Continuous Delivery/Deployment (CI/CD) by automating repetitive tasks such as building, testing, and deploying applications.

The relationship between GitHub and Jenkins was also studied. GitHub is used to store and manage source code, while Jenkins can monitor a repository and execute configured automation tasks when changes are detected or a pipeline is triggered.

Practical learning included creating Jenkins Freestyle Projects, implementing basic Jenkins Pipelines, and understanding Groovy, the scripting language commonly used to define Jenkins pipeline logic. The session also introduced the Jenkinsfile and its role in storing pipeline definitions alongside project source code.

## 2. Topics Covered

### 2.1 Introduction to Jenkins

Jenkins is an open-source automation server used to automate tasks throughout the software development lifecycle.

In a typical software project, developers regularly modify code, build applications, run tests, and prepare releases. Performing all these activities manually can consume time and introduce inconsistencies.

Jenkins helps automate these tasks by executing configured jobs and pipelines.

#### Why Jenkins Is Used

- **Build Automation:** Jenkins can build an application whenever a job or pipeline is triggered.
- **Automated Testing:** It can execute configured test commands to check application behavior.
- **Continuous Integration:** Jenkins can integrate with version control platforms to validate code changes.
- **Deployment Automation:** It can execute configured steps to deploy applications to supported environments.
- **Workflow Automation:** It can organize multiple development tasks into a repeatable sequence.
- **Tool Integration:** Jenkins supports integration with version control systems, build tools, testing frameworks, containerization tools, and deployment platforms.

Jenkins is useful because it reduces repetitive manual work and helps make software delivery more consistent.

### 2.2 Understanding the Relationship Between GitHub and Jenkins

GitHub and Jenkins serve different but complementary purposes in a DevOps workflow.

**GitHub** is a platform for hosting Git repositories. It stores source code, maintains project history, and supports collaboration between developers.

**Jenkins** is an automation server that can retrieve code from a repository and execute configured build, testing, and deployment tasks.

#### How They Work Together

A basic GitHub–Jenkins workflow can operate as follows:

1. A developer modifies the application's source code.
2. The changes are committed and pushed to a GitHub repository.
3. Jenkins detects the changes through a configured webhook, polling mechanism, or another trigger.
4. Jenkins retrieves the required source code.
5. Jenkins executes the configured build steps.
6. Automated tests may run to validate the application.
7. If the pipeline is configured for deployment, Jenkins can deploy the application after the required checks succeed.

The exact workflow depends on the job configuration, available tools, credentials, and deployment requirements.

#### Difference Between GitHub and Jenkins

| Basis of Difference | GitHub | Jenkins |
|---|---|---|
| Primary Purpose | GitHub hosts source code and supports version control collaboration. | Jenkins automates software development and delivery tasks. |
| Main Function | It manages repositories, commits, branches, and pull requests. | It executes configured jobs and pipelines for building, testing, and deployment. |
| Role in CI/CD | It acts as a source code repository and can trigger external automation. | It retrieves source code and runs the configured automation workflow. |
| Workflow | Developers use it to manage and share code changes. | Developers and teams use it to automate repetitive development tasks. |
| Integration | GitHub can send events or provide repository access to Jenkins. | Jenkins can connect to GitHub and other tools to automate workflows. |

### 2.3 Importance of Jenkins in DevOps

Jenkins is important in DevOps because it helps connect code changes with automated validation and delivery processes.

Without automation, developers or operations teams may need to repeat the same build, test, and deployment steps manually for each release.

Jenkins can help by:

- Reducing repetitive manual tasks.
- Executing workflows in a defined order.
- Providing build and pipeline execution history.
- Identifying failures during automated processes.
- Supporting frequent integration of code changes.
- Integrating with tools used for testing, containerization, and deployment.

Jenkins does not automatically know how an application should be built or deployed. The required tools, commands, credentials, and workflow steps must be configured appropriately.

### 2.4 Jenkins Freestyle Projects

A **Freestyle Project** is a basic type of Jenkins job that allows users to configure build tasks through the Jenkins web interface.

It is useful for learning Jenkins fundamentals because users can configure a job without initially writing a complete pipeline script.

A Freestyle Project can be configured to retrieve source code, execute build commands, run tests, and perform other supported build actions.

#### Main Configuration Areas

Depending on the Jenkins installation and available plugins, a Freestyle Project may include:

- **Source Code Management:** Specifies where the project source code is stored, such as a Git repository.
- **Build Triggers:** Defines when Jenkins should run the job.
- **Build Environment:** Configures relevant settings for the build process.
- **Build Steps:** Specifies commands or actions Jenkins should execute.
- **Post-Build Actions:** Defines additional actions to perform after the build, such as publishing results or triggering another job.

#### Example Workflow

A simple Freestyle Project could be configured to:

1. Retrieve source code from GitHub.
2. Execute a build command.
3. Run configured tests.
4. Display the build result in Jenkins.

The steps depend on the application and the tools installed on the Jenkins environment.

During the session, Freestyle Projects were created to understand how Jenkins jobs are configured and executed.

### 2.5 Introduction to Jenkins Pipelines

A **Jenkins Pipeline** is a way to define a sequence of automated software delivery steps.

Instead of configuring every step separately through a graphical interface, pipeline logic can be written as code. This makes the workflow easier to review, maintain, share, and version alongside the application.

A pipeline may contain stages for retrieving source code, building the application, running tests, and deploying the resulting artifact.

#### Common Pipeline Stages

- **Checkout:** Retrieves the required source code from version control.
- **Build:** Compiles or packages the application, depending on the technology.
- **Test:** Executes automated tests.
- **Deploy:** Releases the application to the configured environment when the required conditions are satisfied.

Not every pipeline requires all these stages. The stages depend on the project's needs.

#### Advantages of Jenkins Pipelines

- **Repeatability:** The same defined workflow can be executed repeatedly.
- **Version Control:** Pipeline definitions can be stored in the project repository.
- **Visibility:** Jenkins provides execution status and logs for pipeline stages.
- **Maintainability:** Changes to the workflow can be reviewed and tracked.
- **Automation:** Multiple development tasks can be connected into a single process.

Basic Jenkins Pipelines were implemented during the session to understand how pipeline stages organize automation tasks.

### 2.6 Introduction to Groovy

Groovy is a programming and scripting language that runs on the Java platform. Jenkins uses Groovy-based syntax for defining many Pipeline scripts.

Groovy supports variables, strings, conditional statements, loops, functions, and other programming constructs. These features allow Jenkins pipeline definitions to express the logic needed to control an automated workflow.

#### Example of a Simple Groovy Statement

```groovy
def message = "Hello from Jenkins"
println(message)
```

In this example:

- `def` declares a variable.
- `message` is the variable name.
- The text inside quotation marks is a string.
- `println()` prints the message.

Jenkins Pipeline scripts use Groovy-based syntax together with Jenkins-specific Pipeline steps and objects. Therefore, writing a Jenkinsfile involves more than writing an ordinary standalone Groovy script.

### 2.7 Understanding the Jenkinsfile

A **Jenkinsfile** is a text file that defines a Jenkins Pipeline.

It allows the pipeline configuration to be maintained as code rather than being stored only in a job's graphical configuration.

A Jenkinsfile is commonly stored in the root directory of the project's repository, although Jenkins can be configured to use a different path.

When a Pipeline job is configured to use a repository-based Jenkinsfile, Jenkins retrieves the file and interprets its pipeline definition during execution.

#### Benefits of a Jenkinsfile

- **Pipeline as Code:** The workflow is defined in a version-controlled file.
- **Change Tracking:** Git records modifications to the pipeline definition.
- **Collaboration:** Team members can review and modify pipeline changes.
- **Repeatability:** The pipeline definition can be reused across executions.
- **Maintainability:** Pipeline logic is stored alongside the application code.

### 2.8 Basic Structure of a Jenkinsfile

Jenkins supports Declarative and Scripted Pipeline syntax. Declarative Pipeline provides a structured format that is often easier for beginners to read.

The following example illustrates a simple Declarative Jenkinsfile:

```groovy
pipeline {
    agent any

    stages {
        stage('Development') {
            steps {
                echo 'Source code stage'
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage'
            }
        }

        stage('Testing') {
            steps {
                echo 'Testing stage'
            }
        }
    }
}
```

#### Explanation of the Example

**1. `pipeline`**

Defines the overall Pipeline structure.

**2. `agent any`**

Allows Jenkins to run the pipeline on any available suitable agent.

**3. `stages`**

Contains the stages that organize the workflow.

**4. `stage('Development')`**

Defines a named stage. In this illustrative example, it prints a message rather than retrieving actual source code.

**5. `steps`**

Contains the actions Jenkins executes within the stage.

**6. `echo`**

Prints a message in the Jenkins build log.

This example demonstrates the structure of a Jenkinsfile. It does not perform a real build or deploy an application because it contains only demonstration messages.

### 2.9 How Jenkins Executes a Jenkinsfile

A repository-based Jenkins Pipeline generally follows this process:

1. A Jenkins Pipeline job is configured to use a source code repository.
2. Jenkins retrieves the repository and locates the configured Jenkinsfile.
3. Jenkins interprets the pipeline definition.
4. The configured stages and steps are executed on an appropriate Jenkins agent.
5. Jenkins records the execution status and provides logs for reviewing the results.

If a pipeline stage fails, the pipeline may stop or follow configured failure-handling behavior. The result depends on the pipeline definition.

Storing the Jenkinsfile in version control helps teams manage application code and automation logic together.

## 3. Practical Implementation

### 3.1 Creating Jenkins Freestyle Projects

Freestyle Projects were created to understand the basic Jenkins job configuration process and how Jenkins executes configured tasks.

This activity introduced the graphical configuration approach to build automation.

### 3.2 Implementing Basic Jenkins Pipelines

Basic Jenkins Pipelines were implemented to understand how automated workflows are organized into stages and steps.

The exercise introduced pipeline-based automation as an alternative to configuring every task separately through the Jenkins interface.

### 3.3 Exploring Groovy and Jenkinsfiles

The fundamentals of Groovy were studied to understand the scripting syntax used in Jenkins Pipeline definitions.

The role of the Jenkinsfile was also explored, including how it stores pipeline logic in a repository and how Jenkins can retrieve and execute that definition.

## 4. Key Learnings

- Understood what Jenkins is and how it supports CI/CD automation.
- Learned the difference between GitHub's source code hosting role and Jenkins' automation role.
- Understood how Jenkins can retrieve source code and automate configured workflows.
- Created Jenkins Freestyle Projects.
- Implemented basic Jenkins Pipelines.
- Learned the fundamentals of Groovy scripting.
- Understood the purpose and structure of a Jenkinsfile.
- Learned why Jenkinsfiles are commonly stored in the project's root directory.
- Understood how pipeline definitions can be version-controlled alongside application code.

## 5. Learning Outcome

Day 17 provided practical exposure to Jenkins job configuration and pipeline-based automation. The session established how Jenkins can work with GitHub to retrieve source code and automate software development tasks.

Creating Freestyle Projects and basic Pipelines helped demonstrate two approaches to configuring Jenkins workflows. Learning Groovy and Jenkinsfile fundamentals also introduced the concept of Pipeline as Code, where automation logic is stored in a maintainable and version-controlled format.

These concepts provide a foundation for developing more complete CI/CD workflows involving automated builds, testing, Docker image creation, and application deployment.

---

[⬅️ Back to Week 4](README.md) | [⬅️ Back to Main Training Diary](../README.md)
