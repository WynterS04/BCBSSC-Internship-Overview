# Jenkins Pipeline Overview

This overview of Jenkins Pipeline highlights some of its key concepts, benefits, and functionalities.

## Introduction to Jenkins  
### What is it?
Jenkins pipeline is a suite of plugins that define and automate CI/CD (Continuous Integration/Continuous Delivery) workflows.

Simply put, Jenkins automates the process needed for new code to go from version control (ex: GitHub) to full deployment (servers, production, etc.), where users can actually access it.

### How does it work?
Jenkins uses Groovy, a Pipeline DSL (Domain-specific Language), to define a code-based sequence of steps that dictate what happens after code is pushed and in what order to do so.

Think of Jenkins as a numbered list. As soon as new code is pushed, it implements the insructions outlined in that list automatically, with little human intervention needed.

## Key Features
A pipeline can be a mental checklist that one follows like pulling code from version control, building the app, running test, and uploading it to a server. But this process is repetitive and time-consuming when done manually. Jenkins, however, has several beneficial features that make this process smoother.

### Code-Based
Jenkinsfiles are code-based and can be included in version control, meaning:
- they can be applied to all branches and PRs
- other team members can easily edit/view them
- they can be iterated/reviewed on Jenkins Pipeline, like regular code

### Durable
- Jenkins remembers states
- can survive planned or unplanned restarts

### Automated
- automates repetitive tasks like building, testing, and deploying code
- can optionally allow human intervention when needed (ex: get developer signoff before deployment)

### Versatile
- supports parallelism at 2 levels (can run multiple Jenkinsfiles at once and run stages in the same Jenkinsfile concurrently)
- automatically starts tasks after code changes

### Extensible
- plugins add new capabilities allowing Jenkins to "talk" to other tools
- offers customizable plugins and code for Jenkinsfile

## Declarative vs. Scripted Pipelines
Jenkins uses two types of syntax for witten code: Declarative and Scripted

### Declarative Pipeline
- uses predefined sections to structure code (think of filling out a form)
- simple and structured, but more restrictive
- easier to read and maintain
- must start with pipeline block

**Declarative Pipeline Example:**
```Groovy
pipeline {
    stages{
        stage('Build') {
            steps{
                ''
            }
        }

        stage('Test') {
            steps{
                ''
            }
        }

        stage('Deploy') {
            steps{
                ''
            }
        }
    }
}
```

### Scripted Pipeline
- allows developers to make their own code
- less restrictive, programming-style pipeline
- gives developers full control over process
- must start with node block

**Scripted Pipeline Example:**
```Groovy
node {
    stage('Build'){
        ''
    }

    stage('Test'){
        ''
    }

    stage('Deploy'){
        ''
    }
}
```

## References
[Jenkins User Documentation](https://www.jenkins.io/doc/book/pipeline/)