# How the usage of Git, Docker, automated testing, and continuous integration can improve the productivity and competitiveness of a company?

In this document
* [Introduction](#introduction)
* [Docker](#docker)
* [Continuous Integration](#continuous-integration)
* [Automated Testing](#automated-testing)
* [Sources and Useful Links](#sources-and-useful-links)

## Introduction

We already know about the different benefits of using a GIT repository:
* Developers can keep track of the changes to their code and revert broken/erroneous code.
* Multiple developers can easily work on the same project at the same time.
* Multiple versions of an application can be maintained, such as production, release, development, features etc without adding increased complexity.

GIT really shines when it forms part of a teams development process from development and testing to deployment.
* The entire life-cycle can be automated:
    * Containerization tools like Docker and Vagrant can ensure a consistent environment during development, testing and deployment.
    * automatic testing frameworks like Jenkins and Selenium can perform automated tests without user intervention
    * and Continuous Integration frameworks like those provided by CircleCI and AWS link everything together to work as a well-oiled machine.
* Why is automation such a good idea? The fact is that humans make mistakes:
    * A tester might forget to run a test that prevents him from approving buggy code.
    * A developer may forget to commit a change for a critical bug
    * The overworked sysadmin missed his morning cup of caffeine and deployed the wrong code and now clients are angrily ringing up the CEO.
* Another major reason for this type of automation is speed, the time required to go from an idea to a production-ready commercial application can now be greatly reduced, leading to increased efficiency.

Lets explore the individual components of thisw approach

## Docker

* Every developer has their own prefered way of writing code
    * Alice prefers using Eclipse on a macOS
    * Bob prefers vim on Ubuntu 1804
    * Charlie prefers VS Code on Windows 10
* The problem is that the actual production server runs an old version of Ubuntu Server
* This inevitably means that errors are likely to occur due to inconsistencies caused by different operating systems and application setups.
* Docker allow you to emulate the production environment of an application on a developers system regardless of their operating system or hardware configuration
*Dockers can also be used by automated testing systems to ensure that the testing environment closely matches the production environment in order to be better able to catch bugs and errors.

## Continuous integration

* Is a development practice in which developers integrate code into a shared repository several times a day.
  
* This allows developers to easily integrate functionality with the existing code. 
  
* Automated testing ensured that any commit made to the code does not result in new errors being introduced into production code.

* Some CI systems can also be set up to automatically test the latest code in a docker container when a commit is made


## Automated Testing

* Most modern programming languages such a JavaScript, Java, C# and Python allow for the development of automated tests.
* These are tests that can run without any user intervention and can result in either a pass or a fail result.
* This approach can be used to create multiple tests that can test all aspects of a software application before it can be approved to go into production
* A testing server such as jenkins can therefore act as a gatekeeper that can test an application before it is delivered to the client.

