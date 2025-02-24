# Contributing guidelines

First off, thank you for considering contributing to Kotools Types.

## Bug report

If you've noticed a bug, you can check in the [open issues] if this bug was
already reported by another user.
If this is the case, please react in the corresponding issue for being noticed
when it will be integrated.
If not, please report it by [creating an issue].

> Don't forget to indicate the version and the platform label where the bug was
> encountered.

[creating an issue]: https://github.com/kotools/types/issues/new?assignees=&labels=bug&projects=&template=bug-template.md&title=Bug
[open issues]: https://github.com/kotools/types/issues?q=is%3Aopen+is%3Aissue+label%3Abug

## Feature suggestion

If you have a feature idea or a change request, you can check in the
[open discussions] if your topic was already suggested by another user.
If this is the case, please join the corresponding discussion by commenting or
up-voting it for being noticed when it will be integrated.
If not, please submit it by [creating a dedicated discussion].

A maintainer will create an issue from this discussion if the change request is
approved.

> Don't forget to indicate the platform label where the change could be applied.

[creating a dedicated discussion]: https://github.com/kotools/types/discussions/new?category=ideas&labels=feature
[open discussions]: https://github.com/kotools/types/discussions/categories/ideas?discussions_q=is%3Aopen+category%3AIdeas+sort%3Atop

## Issue implementation

If you would like to implement an issue, please do the following:

1. Notify the maintainers by commenting in the issue that you would like to work
   on it.
2. [Fork Kotools Types].
3. Create a branch from `main` with a name that follows the pattern below.

```text
<type>/<issue-id>
where <type> = feature | bug | documentation | security
and <issue-id> = the issue's identifier
```

For example, if you would like to work on the issue [#31], run the following
command in your terminal:

```shell
git checkout -b feature/31 main
```

[#31]: https://github.com/kotools/types/issues/31
[Fork Kotools Types]: https://github.com/kotools/types/fork

### Requirements

For contributing to this library, we recommend you to use [IntelliJ IDEA] at
least with the Community Edition.
This project contains run and style configurations compatible with this IDE for
facilitating the development process.

> Tip: You can run configurations directly from this documentation if you open
> it in [IntelliJ IDEA].

Also, make sure to have the [Java Development Kit] (JDK) installed on your
machine.
We recommend you to install the JDK 17 if this is not done yet.

[IntelliJ IDEA]: https://www.jetbrains.com/fr-fr/idea
[Java Development Kit]: https://www.oracle.com/fr/java/technologies/downloads

### Running tests

Now that you have opened your fork in [IntelliJ IDEA], you can run the
`JVM tests` configuration for testing the library on the JVM platform.

Here's the list of available configurations for running tests:

- `All tests` for running them on all platforms.
- `JS tests` for running them on the JS platform.
- `JVM tests` for running them on the JVM platform.
- `Linux tests` for running them on the Native platform for Linux.
- `macOS tests` for running them on the Native platform for macOS.
- `Windows tests` for running them on the Native platform for Windows.

### Serving the documentation

You can also generate the documentation by running the `Documentation`
configuration.

> This configuration is continuous, which means that it will update
> automatically the documentation on changes to Kotlin files.

For serving the documentation locally, right-click on the
`build/dokka/index.html` file and choose your favorite browser in the
`Open In > Browser` menu.

### Implementing the issue

At this point, you're ready to make your changes!
Usually, the issue that you chose to work on contains a checklist that you can
use as a reminder.
But if needed, feel free to [ask for help]; everyone is a beginner at first.

[ask for help]: https://github.com/kotools/types/discussions/new?category=q-a

### Checking the API binaries

When introducing changes to the API, you can check its binaries by running the
`Check API binaries` configuration.
This ensures that we are maintaining the binary compatibility of this library.

In some cases, this configuration will fail and will request you to update the
API binaries.
You can do this by running the `Dump API binaries` configuration.

> You can see [what makes a binary incompatible change] to the public API in the
> [Kotlin/binary-compatibility-validator] project.

[Kotlin/binary-compatibility-validator]: https://github.com/Kotlin/binary-compatibility-validator
[what makes a binary incompatible change]: https://github.com/Kotlin/binary-compatibility-validator#what-makes-an-incompatible-change-to-the-public-binary-api

### Committing changes

This project follows the [Conventional Commits] guidelines for committing with
Git.
Please read the specifications for aligning with the project standards.

[Conventional Commits]: https://www.conventionalcommits.org/en/v1.0.0

### Creating a Pull Request

Before creating a [Pull Request] (PR) for submitting your changes to the
maintainers of this library, you should make sure that your `main` branch is
up-to-date with the `main` branch of Kotools Types:

```shell
git remote add upstream git@github.com:kotools/types.git
git checkout main
git pull upstream main
```

Then update your branch from your local copy of `main` and push it!
For example, if you worked on the issue [#31], run the following commands in the
terminal:

```shell
git checkout feature/31
git rebase main
git push -u origin feature/31
```

Finally, go to GitHub and create a PR for integrating your changes in the `main`
branch of Kotools Types.

Because we believe that [quality of code is better than quantity], GitHub
Actions will run our integration workflow for ensuring that your changes work on
all platforms.
Your PR won't be merged until this workflow passes.

A maintainer of Kotools Types will assign itself for reviewing your request.

> Please note that only the maintainer is allowed to merge your PR.

[Pull Request]: https://help.github.com/articles/creating-a-pull-request
[quality of code is better than quantity]: https://github.com/kotools/types#design-goals
