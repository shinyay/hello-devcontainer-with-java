# Hello Dev Containers with Java

This project configures for **Java** development environment on **Dev Containers**.

![image](https://github.com/shinyay/hello-devcontainer-with-java/assets/3072734/d3eb12e4-deb5-4c59-ab58-b2253b616f18)

## Description

## Demo

## Features

- Java 21
- Gradle
- Kotlin
- Ki

## Requirement

- [Visual Studio Code](https://code.visualstudio.com/Download)
- [Docker](https://www.docker.com/)

My environment:

- WSL2 on Windows 11

## Usage

### 0. Notice

You can choose `OpenJDK` or `Microsoft Build of OpenJDK` on `devcontainer.json`

```yaml
// "dockerComposeFile": "compose.yaml",
// "dockerComposeFile": "compose.open.yaml",
```

- `compose.yaml`: **OpenJDK**
- `compose.open.yaml` : **Microsoft Build of OpenJDK**

### 1. Open / Rebuild Dev Container

```shell
Ctrl + p
```

Select the following option:

```text
> Dev Containers: Rebuild and Reopen in Container
```

### 2. Open terminal view

```shell
Ctrl + p
```

Select the following option:

```text
> Terminal: Create New Terminal
```

### 3. Create Java Project with Gradle

Execute the following commands to create and move project directories.

```shell
vscode ➜ /workspace $ mkdir sample
vscode ➜ /workspace $ cd sample/
vscode ➜ /workspace/sample $ gradle init
```

Default choinces are fine. In the following case, I selected **application** type project. Otherwise, source directories are note created by Gradle.

```shell
Select type of project to generate:
  1: basic
  2: application
  3: library
  4: Gradle plugin
Enter selection (default: basic) [1..4] 2

Select implementation language:
  1: C++
  2: Groovy
  3: Java
  4: Kotlin
  5: Scala
  6: Swift
Enter selection (default: Java) [1..6] 

Generate multiple subprojects for application? (default: no) [yes, no] 
Select build script DSL:
  1: Kotlin
  2: Groovy
Enter selection (default: Kotlin) [1..2] 

Select test framework:
  1: JUnit 4
  2: TestNG
  3: Spock
  4: JUnit Jupiter
Enter selection (default: JUnit Jupiter) [1..4]

Project name (default: sample): 
Enter target version of Java (min. 7) (default: 21): 
Generate build using new APIs and behavior (some features may change in the next minor release)? (default: no) [yes, no] 
```

```shell
vscode ➜ /workspace/sample $ tree app
app
├── build.gradle.kts
└── src
    ├── main
    │   ├── java
    │   │   └── org
    │   │       └── example
    │   │           └── App.java
    │   └── resources
    └── test
        ├── java
        │   └── org
        │       └── example
        │           └── AppTest.java
        └── resources
```

## Installation

## References

- [Create a Dev Container](https://code.visualstudio.com/docs/devcontainers/create-dev-container)
- [Development Containers](https://containers.dev/)
  - [devcontainer.json reference](https://containers.dev/implementors/json_reference/)
  - [Development Container Specification](https://containers.dev/implementors/spec/)

- [Dev Containers: Getting Started](https://microsoft.github.io/code-with-engineering-playbook/developer-experience/devcontainers/)

## Licence

Released under the [MIT license](https://gist.githubusercontent.com/shinyay/56e54ee4c0e22db8211e05e70a63247e/raw/34c6fdd50d54aa8e23560c296424aeb61599aa71/LICENSE)

## Author

- github: <https://github.com/shinyay>
- twitter: <https://twitter.com/yanashin18618>
- mastodon: <https://mastodon.social/@yanashin>
