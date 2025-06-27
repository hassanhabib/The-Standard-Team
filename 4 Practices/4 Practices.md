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

| Category               | Description |
|------------------------|-------------|
| INFRA                  | Initial project setup, creating the build project / build scripts. |
| MAJOR INFRA            | Major updates, removing or adding simple configurations or files. |
| MEDIUM INFRA           | Medium updates, removing or adding simple configurations or files. |
| MINOR INFRA            | Minor updates, removing or adding simple configurations or files. |
| PROVISIONS             | Creating provision project / scripts. |
| RELEASES               | Infrastructure work to release software. |
| DATA                   | Creation of a data model (and its migration when EF is used) |
| MAJOR DATA             | Changing existing data model with 5+ property additions/modifications. |
| MEDIUM DATA            | Changing existing data model with 3-4 property additions/modifications. |
| MINOR DATA             | Changing existing data model with 1-2 property additions/modifications. |
| MIGRATION              | Moving or transforming data from one system to another, updating existing data, or generating reports. |
| MAJOR MIGRATION        | Major data migration or transformation tasks involving significant data volume or complexity. |
| MEDIUM MIGRATION       | Medium complexity data migration or updates involving moderate data volume or effort. |
| MINOR MIGRATION        | Minor data migration or simple data updates with low complexity or small data volume. |
| BROKERS                | When creating a broker to wrap external libraries, resources, services, or APIs |
| MAJOR BROKERS          | Major changes to existing broker (significant functionality changes). |
| MEDIUM BROKERS         | Medium changes to existing broker (multiple significant modifications). |
| MINOR BROKERS          | Minor changes to existing broker (simple modifications). |
| FOUNDATIONS            | When creating a Foundation Service |
| MAJOR FOUNDATIONS      | Changing existing foundation service with writing or updating all or to 5+ tests. |
| MEDIUM FOUNDATIONS     | Changing existing foundation service with writing or updating to 3-4 tests. |
| MINOR FOUNDATIONS      | Changing existing foundation service with writing or updating to 1-2 tests. |
| PROCESSINGS            | When creating a Processing Service |
| MAJOR PROCESSINGS      | Changing existing processing service with writing or updating all or to 5+ tests. |
| MEDIUM PROCESSINGS     | Changing existing processing service with writing or updating to 3-4 tests. |
| MINOR PROCESSINGS      | Changing existing processing service with writing or updating to 1-2 tests. |
| ORCHESTRATIONS         | When creating an Orchestration Service |
| MAJOR ORCHESTRATIONS   | Changing existing orchestration service with writing or updating all or to 5+ tests. |
| MEDIUM ORCHESTRATIONS  | Changing existing orchestration service with writing or updating to 3-4 tests. |
| MINOR ORCHESTRATIONS   | Changing existing orchestration service with writing or updating to 1-2 tests. |
| COORDINATIONS          | When creating a Coordination Service |
| MAJOR COORDINATIONS    | Changing existing coordination service with writing or updating all or to 5+ tests. |
| MEDIUM COORDINATIONS   | Changing existing coordination service with writing or updating to 3-4 tests. |
| MINOR COORDINATIONS    | Changing existing coordination service with writing or updating to 1-2 tests. |
| MANAGEMENTS            | When creating a Management Service |
| MAJOR MANAGEMENTS      | Changing existing management service with writing or updating all or to 5+ tests. |
| MEDIUM MANAGEMENTS     | Changing existing management service with writing or updating to 3-4 tests. |
| MINOR MANAGEMENTS      | Changing existing management service with writing or updating to 1-2 tests. |
| AGGREGATIONS           | When creating an Aggregation Service |
| MAJOR AGGREGATIONS     | Changing existing aggregation service with writing or updating all or to 5+ tests. |
| MEDIUM AGGREGATIONS    | Changing existing aggregation service with writing or updating to 3-4 tests. |
| MINOR AGGREGATIONS     | Changing existing aggregation service with writing or updating to 1-2 tests. |
| CONTROLLERS            | When creating a Controller |
| MAJOR CONTROLLERS      | Changing existing controller with writing or updating all or to 5+ tests. |
| MEDIUM CONTROLLERS     | Changing existing controller with writing or updating to 3-4 tests. |
| MINOR CONTROLLERS      | Changing existing controller with writing or updating to 1-2 tests. |
| CLIENTS                | When creating a client on a library that others can use |
| MAJOR CLIENTS          | Changing existing client with writing or updating to 5+ tests. |
| MEDIUM CLIENTS         | Changing existing client with writing or updating to 3-4 tests. |
| MINOR CLIENTS          | Changing existing client with writing or updating to 1-2 tests. |
| PROVIDERS              | When creating a provider on a SPAL provider library that others can use |
| EXPOSERS               | When creating any other kind of exposer i.e. Program.cs |
| MAJOR EXPOSERS         |  |
| MEDIUM EXPOSERS        |  |
| MINOR EXPOSERS         |  |
| VIEWS                  | When creating a View Service |
| MAJOR VIEWS            | Changing existing view with writing or updating all or to 5+ tests. |
| MEDIUM VIEWS           | Changing existing view with writing or updating to 3-4 tests. |
| MINOR VIEWS            | Changing existing view with writing or updating to 1-2 tests. |
| BASES                  | When creating a Frontend Base Component |
| MAJOR BASES            |  |
| MEDIUM BASES           |  |
| MINOR BASES            |  |
| COMPONENTS             | When creating a Component |
| MAJOR COMPONENTS       | Changing existing component with writing or updating all or to 5+ tests. |
| MEDIUM COMPONENTS      | Changing existing component with writing or updating to 3-4 tests. |
| MINOR COMPONENTS       | Changing existing component with writing or updating to 1-2 tests. |
| PAGES                  | When creating a Blazor Page |
| MAJOR PAGES            | |
| MEDIUM PAGES           | |
| MINOR PAGES            | |
| ACCEPTANCE             | When writing an Acceptance Test |
| MAJOR ACCEPTANCE       | |
| MEDIUM ACCEPTANCE      | |
| MINOR ACCEPTANCE       | |
| INTEGRATION            | When writing an Integration Test |
| MAJOR INTEGRATION      | |
| MEDIUM INTEGRATION     | |
| MINOR INTEGRATION      | |
| CODE RUB               | Small change to fix things styling, code formatting, spelling (Not for bug fixes) |
| MAJOR CODE RUB         | Significant code cleanup affecting multiple files. |
| MEDIUM CODE RUB        | Moderate code cleanup affecting several files. |
| MINOR CODE RUB         | Minor code cleanup affecting few files. |
| MINOR FIX              | A minor bug fix / change that do not significantly alter the overall functionality of the program. |
| MEDIUM FIX             | A fix that has a moderate level of impact on the functionality or performance of a program or system. |
| MAJOR FIX              | A major bug fix is a significant repair or correction made to a software program or system that addresses a critical or major issue. |
| DOCUMENTATION          | General documentation |
| CONFIG                 | Any configuration changes i.e. setting up appsettings.json for your various environments. |
| REVIEW                 | Reviewing submitted work in the context of project standards, and Standard compliance. |
| STANDARD               | When you update or introduce a new thing in The Standard |
| DESIGN                 | Creating documentation has design details for your architecture (High Level Design / Low Level Design) |
| MAJOR DESIGN           | Designing 15+ service methods. |
| MEDIUM DESIGN          | Designing 10-14 service methods. |
| MINOR DESIGN           | Designing <10 service methods. |
| BUSINESS               | Creating documentation that outlines your business processes / Standard Operating Procedures. |
| IMPORT                 | When you are copying code and tests over from another system with no or minor changes like namespaces. Should include the component being imported, format: IMPORT: [COMPONENT]: [Description] |
| STATUS                 | When updating STATUS information in your design documentation. |
| PLANNING               | Planning should occur once per feature and involve collaboration across services. Individual work and planning for themselves doesn't quality as planning. Planning involves multiple engineers with a leader who assigns and distributes the tasks across the team. |
| MAJOR PLANNING         | Planning 10+ tasks. |
| MEDIUM PLANNING        | Planning 5+ tasks. |
| MINOR PLANNING         | Planning <5 tasks. |
| MENTORSHIP             | 60+ minute session. |
| MAJOR MENTORSHIP       | 60+ minute session. |
| MEDIUM MENTORSHIP      | 45 minute session. |
| MINOR MENTORSHIP       | 30 minute session. |
| DISCUSSION             | When conducting a discussion meeting under the DISCUSSION title, surrounding technical issues. |
| MAJOR DISCUSSION       | 60+ minute discussion. |
| MEDIUM DISCUSSION      | 45 minute discussion. |
| MINOR DISCUSSION       | 30 minute discussion. |

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


### 4.1.5 Configurations

Configuration settings are values that determine the behavior of a software application. 
They can include anything from database connection strings and API keys to feature flags and logging levels. 
By using configuration settings, developers can customize the behavior of their application without modifying the code, 
making it easier to deploy and manage different environments.

One popular way of storing configuration settings in .NET applications is by using the `appsettings.json` file. 
This file is a JSON-formatted file that contains a set of key-value pairs representing configuration settings. 
Developers can easily modify these settings to change the behavior of their application.

However, not all configuration settings can be safely stored in `appsettings.json` files. 
Sensitive data, such as API keys, database passwords, or any other data that could grant 
unauthorized access to the application or its resources, should be kept secret. 
Storing sensitive data in configuration files, especially in plain text format, can put the application's security at risk.

It is very important for developers to follow secure coding practices and never store passwords 
or other sensitive data in configuration provider code or in plain text configuration files. 
Such sensitive data should be stored in a secure location like Azure Key Vault or in environment 
variables that are set in a deployment environment. Storing passwords in local settings files is also 
not recommended as this can easily lead to scenarios where passwords are accidentally checked into code repositories, 
either because a developer has forgotten to exclude the file from version control or as a result of someone changing 
it and then inadvertently including the sensitive files, putting the application's security at risk.

One way of protecting sensitive data is by using **user secrets**.  User secrets is a feature in .NET that provides a 
convenient way for developers to store and retrieve sensitive data during development. 
This data is stored locally on the developer's machine and is not intended to be used in production. 
While user secrets can be useful for keeping sensitive data out of source control and easily accessible during development, 
it is important to note that they are not compatible with GitHub workflow actions. 
Instead, developers should consider using more secure methods for storing secrets, 
such as environment variables or storing them in a secure location like `GitHub Action Secrets` or `Azure Key Vault`.  
As user secrets is not directly compatible with GitHub build pipelines we will not explore this option further.

Another way of protecting sensitive data is the use of **environment variables**. 
Environment variables are variables that are set in the operating system, which can be accessed by applications at runtime. 

By using both **appsettings.json** and **environment variables**, 
developers can separate sensitive data from other configuration settings, 
making it easier to manage and secure. Additionally, 
this approach enables developers to store their configuration settings securely in a build pipeline, 
ensuring that sensitive data is protected throughout the development lifecycle.

#### 4.1.5.1 appsettings.json

A .NET app will be automatically load and register `appsettings.json` and `appsettings.{Environment}.json` with the IConfiguration 
interface during application startup, if the files is located in the application's root directory. 
This means that the key-value pairs defined in the appsettings.json file will be accessible through the IConfiguration object, 
allowing developers to easily access and use the configuration settings throughout their application.

It's worth noting that in addition to the appsettings.json file, there are other configuration providers available in 
.NET that allow developers to load configuration settings from various sources, 
such as environment variables or command-line arguments. 
(Developers can also create their own custom configuration providers to load configuration settings from other sources if needed.)

Configuration sources are read in the order that their configuration providers are specified. 
Order configuration providers in code to suit the priorities for the underlying configuration sources that the app requires.

A typical sequence of configuration providers is:

1. appsettings.json
2. appsettings.{Environment}.json
3. User secrets
4. Environment variables using the Environment Variables configuration provider.
5. Command-line arguments using the Command-line configuration provider.

Lets look at some code samples to see how all this works.

#### 4.1.5.1 Application Settings

**appsettings.json**
```cs
{
  "MySettings": {
    "ApiUrl": "https://api.somesite.com/",    
    "ApiKey": "1ae4e397-ec3c-4ed7-8280-a17d0e2cbe78",
    "OrganisationId": "1bac6df0-cd68-4ce5-9c29-b2beb58201cd"
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft": "Warning",
      "Microsoft.Hosting.Lifetime": "Information"
    }
  },
  "AllowedHosts": "*"
}
```

With the above `appsettings.json` file we can then load our variables like this:
```cs
    string apiUrl = configuration["MySettings:ApiUrl"];
    string apiKey = configuration["MySettings:ApiKey"];
    string organisationId = configuration["MySettings:OrganisationId"];
```
 
#### 4.1.5.2 Environment Variables

We can add environment variables to a web application by doing this:
```cs
var builder = WebApplication.CreateBuilder(args);
...
builder.Configuration.AddEnvironmentVariables();
...
var app = builder.Build();
```

or if you want to play with this in a Console App or Unit Test, you can do this:

```cs
var configurationBuilder = new ConfigurationBuilder()
    .AddJsonFile("appsettings.json", optional: true, reloadOnChange: true)
    .AddEnvironmentVariables("MYAPP_ACCEPTANCE_");

this.configuration = configurationBuilder.Build();
```
**NOTE** that we have defined a prefix that environment variables must start with.  
This prefix will automatically be removed from the environment variabl names by the configuration builder.  
This is a very useful feature as you can now store environment variables with the same name for multiple apps and/or environments.

Up to this point we will still get the same values if we get our config items as we have not set the values for any environment variables yet.

In C# .NET, working with environment variables is straightforward. 
The Environment class provides several methods for reading and setting environment variables. 
For example, to read an environment variable, you can use the `Environment.GetEnvironmentVariable` method, 
passing in the name of the variable you want to retrieve. 
To set an environment variable, you can use the `Environment.SetEnvironmentVariable` method, providing the name of the variable and its value. 
You can also use the command line to set the enviroment variables by running the SETX command.

For demonstration we will leave the value of `MySettings:ApiUrl` in appsettings.json

Next we will set the value of `MySettings:ApiKey` through this line of code
```cs
Environment.SetEnvironmentVariable("MYSETTINGS:APIKEY", "3d4a1c55-fcd7-4b34-8536-99c8ae6ae33c");
```

and for the `MySettings:OrganisationId` we will use the command line argument through a console window with administrative priviledges
```cs
setx MYSETTINGS:APIKEY "b2440ae9-cad2-4d70-b138-4a807abe1bb7"
```
**NOTE**
Visual Studio preloads the environment variables when it starts, and it caches them until the application is closed.  
Unlike environment variables set through code, those set using the command line will not be immediately be available due to the preload behaviour.  
**You will need to close Visual Studio and re-open it.**


Once you have reloaded Visual Studio we can get the values from the configuration again by doing this:
```cs
    string apiUrl = configuration["MySettings:ApiUrl"];
    string apiKey = configuration["MySettings:ApiKey"];
    string organisationId = configuration["MySettings:OrganisationId"];
```

You will notice that the ApiUrl is the same as before, but the values have now changed for `MySettings:ApiKey` and `MySettings:OrganisationId` and they are now equal to the values we specified for the environment variables via code and through SETX on the command line.

You can also remove environment variables through code by setting the value to `null`.
Environment.SetEnvironmentVariable("MYSETTINGS:APIKEY", null);

OR via the command line you can do
```cs
setx MYSETTINGS:APIKEY /delete
```

Or if you prefer a GUI, you can also go to SYSTEM PROPERTES > ENVIRONMENT VARIABLES where you can ADD / REMOVE environment variables.

#### 4.1.5.3 GitHub Actions Workflow

To setup your environment variables for use within GitHub we will need to setup repository secrets and add a section at the beginning of your workflow file.

1. Go to the GitHub repository where you want to use these settings and click on "Settings" in the top navigation bar.

2. In the left sidebar, click on "Secrets" and then click on "New repository secret" button.

3. Create three new secrets named "MYAPP_ACCEPTANCE_MYSETTINGS__APIKEY", and "MYAPP_ACCEPTANCE_MYSETTINGS__ORGANISATIONID", 
respectively, with the corresponding values for "ApiUrl", "ApiKey", and "OrganisationId" from the given settings.  

    **NOTE** 
    * We have prefixed our environment variables with `MYAPP_ACCEPTANCE_` to match the earlier configuration of `.AddEnvironmentVariables("MYAPP_ACCEPTANCE_");`.
    * The other difference is that a colon (:) is not allowed on GitHub Secrets to represent a hierarchy and you have to use a double underscore (__) instead.

4. To expose these secrets as environment variables in the GitHub Action Workflow, add the following code snippet at the beginning of your workflow file:

```yaml
env:
  API_URL: ${{ secrets.MySettings__ApiUrl }}
  API_KEY: ${{ secrets.MySettings__ApiKey }}
  ORG_ID: ${{ secrets.MySettings__OrganisationId }
```

A full example of the `dotnet.yml` file will look like this:
```yaml
name: MyApplication Build
on:
  push:
    branches:
    - main
  pull_request:
    branches:
    - main
jobs:
  build:
    runs-on: windows-latest
    env:
      ApiKey: ${{ secrets.MYAPP_ACCEPTANCE_MYSETTINGS__APIKEY }}
      OrgId: ${{ secrets.MYAPP_ACCEPTANCE_MYSETTINGS__ORGANISATIONID }}
    steps:
    - name: Pulling Code
      uses: actions/checkout@v2
    - name: Installing .NET
      uses: actions/setup-dotnet@v1
      with:
        dotnet-version: 7.0.201
        include-prerelease: false
    - name: Restoring Packages
      run: dotnet restore
    - name: Building Solution
      run: dotnet build --no-restore
    - name: Running Tests
      run: dotnet test --no-build --verbosity normal
```
## 4.2 Measurements
The Standard promotes ideals of fairness to all. The Standard recognizes that innovative ideas, great contributions and high performance is not exclusive to individuals with certain titles. In order to truly and fairly ensure everyone's contributions are measured fairly, The Standard introduces values and points to contributions at different levels and categories. The acculmalations of these contributions increases the rank of the contributor from one level to the next.

### 4.2.0 Contribution Points
The following is a list of all types of contributions and the value for each:
| Title Starts With          | Return Value |
|----------------------------|--------------|
| INFRA                      | 10           |
| MAJOR INFRA                | 10           |
| MEDIUM INFRA               | 3            |
| MINOR INFRA                | 1            |
| DATA                       | 5            |
| MAJOR DATA                 | 5            |
| MEDIUM DATA                | 3            |
| MINOR DATA                 | 1            |
| MIGRATION                  | 20            |
| MAJOR MIGRATION            | 20            |
| MEDIUM MIGRATION           | 10            |
| MINOR MIGRATION            | 5            |
| BROKER                     | 5            |
| MAJOR BROKER               | 5            |
| MEDIUM BROKER              | 3            |
| MINOR BROKER               | 1            |
| FOUNDATION                 | 10           |
| MAJOR FOUNDATION           | 10           |
| MEDIUM FOUNDATION          | 5            |
| MINOR FOUNDATION           | 1            |
| PROCESSING                 | 15           |
| MAJOR PROCESSING           | 15           |
| MEDIUM PROCESSING          | 10           |
| MINOR PROCESSING           | 5            |
| ORCHESTRATION              | 20           |
| MAJOR ORCHESTRATION        | 20           |
| MEDIUM ORCHESTRATION       | 15           |
| MINOR ORCHESTRATION        | 10           |
| COORDINATION               | 20           |
| MAJOR COORDINATION         | 20           |
| MEDIUM COORDINATION        | 15           |
| MINOR COORDINATION         | 5            |
| MANAGEMENT                 | 20           |
| MAJOR MANAGEMENT           | 20           |
| MEDIUM MANAGEMENT          | 15           |
| MINOR MANAGEMENT           | 5            |
| AGGREGATION                | 10           |
| MAJOR AGGREGATION          | 10           |
| MEDIUM AGGREGATION         | 5            |
| MINOR AGGREGATION          | 1            |
| CONTROLLER                 | 5            |
| MAJOR CONTROLLER           | 5            |
| MEDIUM CONTROLLER          | 3            |
| MINOR CONTROLLER           | 1            |
| ACCEPTANCE                 | 10           |
| MAJOR ACCEPTANCE           | 10           |
| MEDIUM ACCEPTANCE          | 5            |
| MINOR ACCEPTANCE           | 3            |
| INTEGRATION                | 15           |
| MAJOR INTEGRATION          | 15           |
| MEDIUM INTEGRATION         | 10           |
| MINOR INTEGRATION          | 10           |
| VIEW                       | 10           |
| MAJOR VIEW                 | 10           |
| MEDIUM VIEW                | 5            |
| MINOR VIEW                 | 1            |
| BASE                       | 5            |
| MAJOR BASE                 | 5            |
| MEDIUM BASE                | 3            |
| MINOR BASE                 | 1            |
| COMPONENT                  | 15           |
| MAJOR COMPONENT            | 15           |
| MEDIUM COMPONENT           | 10           |
| MINOR COMPONENT            | 5            |
| PAGE                       | 5            |
| MAJOR PAGE                 | 5            |
| MEDIUM PAGE                | 3            |
| MINOR PAGE                 | 1            |
| CLIENT                     | 5            |
| MAJOR CLIENT               | 5            |
| MEDIUM CLIENT              | 3            |
| MINOR CLIENT               | 1            |
| EXPOSER                    | 5            |
| MAJOR EXPOSER              | 5            |
| MEDIUM EXPOSER             | 3            |
| MINOR EXPOSER              | 1            |
| DESIGN                     | 20           |
| MAJOR DESIGN               | 20           |
| MEDIUM DESIGN              | 10           |
| MINOR DESIGN               | 5            |
| MAJOR FIX                  | 20           |
| MEDIUM FIX                 | 10           |
| MINOR FIX                  | 5            |
| PLANNING                   | 15           |
| MAJOR PLANNING             | 15           |
| MINOR PLANNING             | 10           |
| MINIOR PLANNING            | 5            |
| MENTORSHIP                 | 20           |
| MAJOR MENTORSHIP           | 20           |
| MINOR MENTORSHIP           | 15           |
| MINIOR MENTORSHIP          | 10           |
| DISCUSSION                 | 15           |
| MAJOR DISCUSSION           | 15           |
| MINOR DISCUSSION           | 10           |
| MINIOR DISCUSSION          | 5            |
| MAJOR CODE RUB             | 10           |
| MEDIUM CODE RUB            | 5            |
| MINOR CODE RUB             | 1            |
| CODE RUB                   | 1            |
| PROVISION                  | 10           |
| IMPORT                     | 5            |
| RELEASE                    | 10           |
| CONFIG                     | 5            |
| REVIEW                     | 1            |
| DOCUMENTATION              | 1            |
| STANDARD                   | 100          |
| BUSINES                    | 50           |
| STATUS                     | 1            |
| UNKNOWN                    | 0            |

Each one of these categories have been defined above in the previous section.

### 4.2.1 Ranks
The following are the ranks based on the life-time accumalation and contribution to The Standard Community and Standard-Compliant projects:
| POSITION            | SCORE           |
|---------------------|-----------------|
| SWE I               | 10,000          |
| SWE II              | 25,000          |
| SR. SWE             | 50,000          |
| PRINCIPAL           | 100,000         |
| PARTNER/DIRECTOR    | 300,000         |
| VP                  | 500,000         |
| DISTINGUISHED       | 1,000,000       |
| THE STANDARD BEARER | 1M + DELEGATION |






