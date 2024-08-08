# Contributing Guidelines

There are two main ways to contribute to the project &mdash; submitting issues and submitting
fixes/changes/improvements via pull requests.

## Issue Submission

Please file the issues [here](https://github.com/Kotlin/kotlin-jupyter-libraries/issues).

General types of issues in this project:
- Descriptor for some library needs to be added
- The library is obsolete and needs to be removed
- The library version is out-of-date
- Descriptor is broken and needs to be fixed

## Submitting Pull Requests

We welcome Pull Requests.
You can submit them [here](https://github.com/Kotlin/kotlin-jupyter-libraries/pulls).

Some rules apply to the pull requests:
- If the pull request fixes an issue, please mention it in the pull request title and in the commit message, i.e.
`Fix #123`
- If the pull request adds a new library, please check the following things:
  - `description` and `link` are present in the descriptor. We generate the list of libraries using these values
  so ensure they are correct
  - `properties` property is present in the descriptor. It should include all versions of Maven dependencies that are
  used in `dependencies` section. It should also include hints for the auto-update of these dependencies. I.e.:
  ```json
  {
    "properties": [
      { "name": "v", "value": "0.1.2" },
      { "name": "v-renovate-hint", "value": "update: package=<group>:<artifact>" }
    ]
  }
  ```
  - at least one dependency is present in the `dependencies` list. Version should be a property reference, i.e.
  `<group>:<artifact>:$v`
  - Other rules and approaches could be found in [this guide](https://github.com/Kotlin/kotlin-jupyter/blob/master/docs/libraries.md)

## Contacting maintainers

If you encounter any issues or have questions about the project, there are several ways to contact the maintainers:

* Submit an [issue](#issue-submission) on GitHub to report a bug or request a new feature.
* Mention the maintainer (@ileasile) on GitHub to draw their attention
  to a specific problem or ask a question.
* For general inquiries and discussions, use the `#notebooks` channel on
  the [KotlinLang Slack](https://kotl.in/slack).
