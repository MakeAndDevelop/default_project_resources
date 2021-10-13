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

### Pull Requests (PR)
The PR flow is an extensions to the flows described above.
* Directly pushing to develop branch and master branch is prohibited and enforced by branch policies.
* Feature/Bugfix/Hotfix branches are merged in respectivally develop and master branch with Pull Requests.
* Pull Request are reviewed by at least two other developers, if the team size allows for this.

## Coding Guidelines
We code in compliance to the Google guidelines, conventions and standards for Dart development:
* [Effective Dart style](https://dart.dev/guides/language/effective-dart/style)

We enforce these guidelines by linting with the current configuration:
* [Official flutter linting config](https://github.com/flutter/packages/blob/master/packages/flutter_lints/lib/flutter.yaml)
