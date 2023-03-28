# 4. Practices

Having defined practices for code contributions, branch, commit strategies and project structures is essential for any software development project. 
These practices provide a clear and consistent approach to managing the codebase, ensuring that contributions are made in a controlled and organized manner. 
This helps to avoid confusion and conflicts, and ensures that the codebase remains stable and maintainable. 
Additionally, well-defined practices for code contributions and project structure can help to improve collaboration and communication within the development team, making it easier to track and review changes, and to identify and resolve issues. 
Overall, defined practices for code contributions, branching and commit strategies as well as project structures are a key part of any successful software development project.

Practices requires these main aspects to be considered:

4. Code Contribution
   1. Forking / Cloning and Branching
   2. Project Structure
   3. Commits
   4. Pull Requests

The Standard Team is to clearly understand and define each and every aspect of the aforementioned points. 

## 4.1 Code Contribution

Defining a contribution guideline is crucial for any open-source or collaborative software development project. 
It establishes clear rules and expectations for how contributors should submit and review changes, which helps to ensure that all contributions are made in a consistent and organized manner. 
Additionally, a contribute guideline can provide guidance on best practices for coding, testing and documentation, which can help to improve the overall quality of the codebase. 
It also serves as an educational tool to new contributors, providing them with the necessary information and instructions on how to contribute to the project effectively. 
(Furthermore, having a well-defined GitHub contribute guideline can help to attract new contributors and maintain a healthy open-source community.)

### 4.1.1 Forking and Branching Strategies
A branch strategy for code is essential for maintaining a stable and maintainable codebase. 
It allows for multiple developers to work on different features or bug fixes simultaneously, without interfering with each other's work. 
Each developer can create their own branch to work on, which can then be merged into the main branch once it has been reviewed and approved. 
This helps to avoid conflicts, and ensures that the codebase remains stable and consistent. 
Furthermore, a branch strategy enables version control and allows different versions of the codebase to be created and tracked. 
This can be useful for rolling back changes if necessary, and for maintaining multiple versions of the software for different environments. 
Overall, a branch strategy is a critical aspect of any software development project and is essential for ensuring that the codebase remains stable and maintainable.

There are several different types of branching strategies that can be used in software development, including:

1. Gitflow: A popular branching strategy that follows a strict branching model, where development happens in feature branches and is merged into a main development branch. This strategy is good for large projects with many contributors.

2. Trunk-Based Development: This strategy involves working on the main branch, or trunk, and committing changes directly to it. This is a good strategy for smaller projects with a small number of contributors.

3. Feature Branching: This strategy involves creating a separate branch for each feature or bug fix, and merging it into the main branch when it is complete. This is a good strategy for larger projects with multiple contributors.

4. Forking: This strategy involves creating a copy of the repository and working on it separately. This is good for open-source projects where multiple contributors are working on the same codebase.  The main advantage of the Forking workflow is that contributions can be integrated without the need for everybody to push to a single central repository. Developers push to their own server-side repositories, and only the project maintainer can push to the official repository. This allows the maintainer to accept commits from any developer without giving them write access to the official codebase.

5. Release Branching: This strategy involves creating a separate branch for each release, and merging it into the main branch when it is ready to be released. This is a good strategy for projects that have a regular release schedule.

6. Continuous Integration: This strategy involves merging code changes as soon as they are made, and running automated tests to ensure that the codebase remains stable. This is a good strategy for projects that have a high frequency of changes.

Ultimately, it's important to choose a branching strategy that fits the needs and constraints of the project, and that can be easily understood and followed by all the contributors.

#### 4.1.1.1 Open Source Development
As The Standard promotes open-source work, lets look have a quick look at the Forking strategy.

**How it works**

The Forking workflow begins with an official public repository stored on a server. When a new developer wants to start working on the project, they do not directly clone the official repository.

Instead, they fork the official repository to create a copy of it. This new copy serves as their personal public repository.  
After they have created their server-side copy, the developer performs a git clone to get a copy of it onto their local machine. 
This serves as their private development environment, just like in the other workflows.

When they're ready to publish a local commit, they push the commit to their own public repository (not the official one). 
They then file a pull request with the main repository, which lets the project maintainer know that an update is ready to be integrated. 
The pull request can then be reviewed and it also serves as a convenient discussion thread if there are issues with the contributed code. 

The following is a step-by-step example of this workflow:

1. A developer 'forks' an 'official' server-side repository. This creates their own server-side copy.
2. The new server-side copy is cloned to their local system.
3. A new local feature branch is created.
4. The developer makes changes on the new branch.
5. New commits are created for the changes.
6. The branch gets pushed to the developer's own server-side copy.
7. The developer opens a pull request from the new branch to the 'official' repository.
8. The pull request gets reviewed and build success and tests are verified.  At this point the maintainer can either request changes or approve for merge upon which the changes are then merged into the original server-side repository.


#### 4.1.1.2 Branch Name Conventions

For branch names we can apply the following naming convention: `users/[username]/[category]-[entity]-[action]`

The variables can be subsituted
* `[username]` => your github username
* `[category]` => the category that you are working on
* `[entity]` => the entity that your service / broker uses
* `[action]` => the action

### 4.1.1.3 Category List

| Category       | Description |
| -------------- | ----------- |
| INFRA          | Initial project setup, creating the build project / build scripts.                   |
| PROVISIONS     | Creating your provions project / scripts.                                            |
| RELEASES       | Infrastructure work to release software.                                             |
| DATA           | Creation of a data model (and its migration when EF is used)                         |
| BROKERS        | When creating brokers to wrap external libraries, resources, services, or APIs       |
| FOUNDATIONS    | When creating Foundation Services                                                    |
| PROCESSINGS    | When creating Processing Services                                                    |
| ORCHESTRATIONS | When creating Orchestration Services                                                 |
| COORDINATIONS  | When creating Coordination Services                                                  |
| MANAGEMENTS    | When creating Management Services                                                    |
| AGGREGATIONS   | When creating Aggregation Services                                                   |
| CONTROLLERS    | When creating an exposer like a REST API                                             |
| CLIENTS        | When creating an exposer on a library that others can use                            |
| EXPOSERS       | When creating any other kind of exposer i.e. Program.cs                              |
| BASE           | When creating frontend base components                                               |
| COMPONENTS     | When creating component                                                              |
| VIEWS          | When working on views                                                                |
| PAGES          | When creating Blazor pages                                                           |
| ACCEPTANCE     | When writing Acceptance Tests                                                        |
| INTEGRATIONS   | When writing Integration Tests                                                       |
| CODE RUB       | Small change to fix things styling, code formatting, spelling  (Not for bug fixes)                       |
| MINOR FIX      | A minor bug fix / change that do not significantly alter the overall functionality of the program.       |
| MEDIUM FIX     | A fix that has a moderate level of impact on the functionality or performance of a program or system.  It may cause some inconvenience or minor disruption to the user experience, but it is not critical and can typically be resolved with a moderate amount of effort.  |
| MAJOR FIX      | A major bug fix is a significant repair or correction made to a software program or system that addresses a critical or major issue that is preventing the program or system from functioning correctly. This type of bug fix is typically classified as high priority, as it affects the overall functionality and usability of the program or system, and can have a significant impact on the user experience. Major bug fixes often require extensive testing and validation before they can be released.           |
| DOCUMENTATION  | General documentation |
| CONFIG         | Any configuration changes i.e. setting up appsettings.json for your various environments.    |
| STANDARD       | When you update or introduce a new thing in The Standard           |
| DESIGN         | Creating doumentation has design details for your architecture (High Level Design / Low Level Design)    |
| BUSINESS       | Creating documentation that outlines your business processes / Standard Operating Procedures.  Work required to bring the customer to use your software. |

### 4.1.2 Projects

Visual Studio utilizes a hierarchical project structure that allows developers to organize their code and resources in a logical and easy-to-navigate manner. 
At the top level, you have a solution that is a container for one one more projetcs. 
A project is the container for all of the files and resources that make up an application.


#### 4.1.2.1 Projects In The Solution

A typical solution structure would look like this...

```
  |-- Taarafo.Core                              (API)
  |-- Taarafo.Core.Infrastructure.Build         (Console App)
  |-- Taarafo.Core.Infrastructure.Provision     (Console App)
  |-- Taarafo.Core.Tests.Acceptance             (xUnit Test Project)
  |-- Taarafo.Core.Tests.Build                  (xUnit Test Project)
```

#### 4.1.2.1 Project Structure 

A typical procect folder structure would look like this...

```
Taarafo.Core
  |-- Brokers
        |-- DateTimes
        |-- Loggings
        |-- Storages
  |-- Models
        |-- Foundations
            |-- Posts
               |-- Exceptions
            |-- Comments
               |-- Exceptions
  |-- Migrations
  |-- Services
        |-- Foundations
            |-- Students
        |-- Processings
            |-- Students
        |-- Orchestrations
            |-- Students
  |-- Controllers
```

The above folder structure can also be carried over into the test projects to organsise models 
and to group the various tests by Services\\`[Service Type]`\\`[ServiceName]`


### 4.1.3 Commits

The Standard follows a TDD (Test-Driven Development) software development methodology that emphasizes writing tests before writing the actual code. 
It is a process of writing a test case, running it and observing it failing, then writing the code to pass the test. 
It's an iterative process that helps developers to focus on the requirements, design, and implementation of the code. 
When using TDD, developers write test cases using a testing framework such as xUnit or NUnit, and use the framework to run and assert the tests. 
The goal is to have a high percentage of test coverage, ensuring that the code is thoroughly tested and any bugs or issues are caught early on in the development process. 
This approach helps to ensure that the code is maintainable, easy to understand, and that it meets the requirements of the project.

When following this TDD process of writing a test case we can use the test name and its outcome to commit the work.
The work done to write the test and observing it failing can be committed as `[Test Name] -> FAIL`  e.g. `ShouldAddPostAsync -> FAIL` 
and subsequently the work done to make it pass can be committed as `[Test Name] -> PASS`  e.g. `ShouldAddPostAsync -> PASS` 

If you are working on any code that does not require testing i.e. DATA, BROKERS, CONTROLLERS, then we would adopt the same naming convention as used for Pull Requests
which uses the category and a description of the work done using this syntax `[CATEGORY]: [Description Of Work Completed]`, where the category is always in CAPS and the description in Pascal Case
e.g.  `DATA: Add Student Model` OR `BROKERS: Insert Student` OR `CONTROLLERS: POST Student`  (See the category table above for a complete list of categories)

### 4.1.4 Pull Requests

When developers have completed their work, they can create a pull request with the main repository, which lets the project maintainer know that an update is ready to be integrated. 
The Pull Request (PR) can be created with the name using this syntax `[CATEGORY]: [Description Of Work Completed]`, where the category is always in CAPS and the description in Pascal Case
e.g. `FOUNDATIONS: Add Student`

The comment section of the PR can also be completed with any additional information that describe the work done and that can be helpfull / relevant to the approver.
e.g. a screenhots of the CONTROLLER actions working as expected showing the various response outcomes like `201 - Created` or `400 - Bad Request` or `424 - Failed Dependency` etc.

You can also link a pull request to an issue to show that a fix is in progress and to automatically close the issue when the pull request or branch is merged by adding a KEYWORD #ISSUE-NUMBER anywhere in the comment section.
e.g. `Closes #10` or if the PR cover multiple things, then you could do `Closes #10, closes #123`

If you simply wish to link an issue without a closing action on merge, you can omit the keyword and just add #ISSUE-NUMBER e.g. `#10`
