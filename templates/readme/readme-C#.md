## Source Control en Pull Requests
We use [git](https://git-scm.com/) for our version control.

### Branching Model
With explicity versioned software, like mobile apps and desktop apps, we use the git-flow:
* [Git-flow](https://nvie.com/posts/a-successful-git-branching-model/)

  Summary:
  * Master branch is used to represent the current state of production
  * Master branch contains Tags e.g. `1.0.0` for each released version so we can always roll back.
  * Develop branch represent the current state of development; completed features and bugfixes.
  * Feature branches are used to develop new features. In large features Task branches can be used.
  * Bugfix branches are used to fix bugs on develop
  * Hotfix branches are used to fix bugs on production/master.
  * Release branches are used to prepare all release related work.
  * Once a release branch is merged in master a tag is created for that version.

In continious deliverd web apps we use the github-flow:
* [Github-flow](https://guides.github.com/introduction/flow/)

### Pull Requests (PR)
The PR flow is an extensions to the flows described above.
* Directly pushing to develop branch and master branch is prohibited by branch policies.
* Feature/Bugfix/Hotfix branches are merged in respectivally develop and master branch with Pull Requests.
* Pull Request are reviewed by at least two other developers, if the team size allows for this.

## Coding Guidelines
We code in compliance to the Microsoft guidelines, conventions and standards for C# development. These guidelines are:

* [C# Coding conventions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/coding-conventions)
* [Naming guidelines](https://docs.microsoft.com/en-us/dotnet/standard/design-guidelines/naming-guidelines)
* [C# Coding standards](http://www.dofactory.com/reference/csharp-coding-standards)

These are enforced with:
* [EditorConfig](https://github.com/MakeAndDevelop/default_project_resources/blob/main/linting/.editorconfig)
* [EditorConfig AzureDevOps integration](https://pumpingco.de/blog/check-if-pull-requests-violate-editorconfig-rules-with-azure-devops-pipelines/)
