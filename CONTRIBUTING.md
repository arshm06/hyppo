# Contributing

(adopted from graspologic)

This project welcomes contributions and suggestions and has adopted the [Neurodata Code of Conduct](https://neurodata.io/about/codeofconduct/).

## Issue Submission (Bug or Feature)

We use GitHub issues to track all bugs and feature requests; feel free to open an issue if you have found a bug or wish
to see a feature implemented. Please also feel free to tag one of the core
contributors (see our [Roles page](https://github.com/neurodata/hyppo/blob/main/ROLES.md)).

In case you experience issues using this package, do not hesitate to submit a ticket to our
[Issue Tracker](https://github.com/neurodata/hyppo/issues).  You are also welcome to post feature requests or pull
requests.

It is recommended to check that your issue complies with the following rules before submitting:

- Verify that your issue is not being currently addressed by other
  [issues](https://github.com/neurodata/hyppo/issues) or
  [pull requests](https://github.com/neurodata/hyppo/pulls).

- If you are submitting a bug report, we strongly encourage you to follow the guidelines in
  [How to create an actionable bug report](#how-to-create-an-actionable-bug-report)

### How to create an actionable bug report

When you submit an issue to [Github](https://github.com/neurodata/hyppo/issues), please do your best to
follow these guidelines! This will make it a lot faster for us to respond to your issue.

- The ideal bug report contains a **short reproducible code snippet**, this way
  anyone can try to reproduce the bug easily (see [this](https://stackoverflow.com/help/mcve) for more details).
  If your snippet is longer than around 50 lines, please link to a [gist](https://gist.github.com) or a github repo.

- If not feasible to include a reproducible snippet, please be specific about
  what **tests and/or functions are involved and the shape of the data**.

- If an exception is raised, please **provide the full traceback**.

- Please include your **operating system type and version number**, as well as
  your **Python and hyppo versions**. This information
  can be found by running the following code snippet:

    ```python
    import platform; print(platform.platform())
    import sys; print(f"Python {sys.version}")
    import hyppo; print(f"hyppo {hyppo.__version__}")
    ```

- Please ensure all **code snippets and error messages are formatted in
  appropriate code blocks**.  See
  [Creating and highlighting code blocks](https://help.github.com/articles/creating-and-highlighting-code-blocks)
  for more details.

## Contributing Code

### Git workflow

The preferred workflow for contributing to hyppo is to fork the main repository on GitHub, clone, and develop on a
branch. Steps:

1. Fork the [project repository](https://github.com/neurodata/hyppo) by clicking on the ‘Fork’ button near the top
   right of the page. This creates a copy of the code under your GitHub user account. For more details on how to
   fork a repository see [this guide](https://help.github.com/articles/fork-a-repo/).

2. Clone your fork of the hyppo repo from your GitHub account to your local disk:

   ```sh
   git clone git@github.com:YourGithubAccount/hyppo.git
   cd hyppo
   ```

3. Create a feature branch to hold your development changes:

   ```sh
   git checkout -b my-feature
   ```

   Always use a `feature` branch. Pull requests directly to either `dev` or `main` will be rejected
   until you create a feature branch based on `dev`.

4. Develop the feature on your feature branch. Add changed files using `git add` and then `git commit` files:

   ```sh
   git add modified_files
   git commit
   ```

   After making all local changes, you will want to push your changes to your fork:

   ```sh
   git push -u origin my-feature
   ```

### Pull Request Checklist

We recommended that your contribution complies with the following rules before you submit a pull request:

- Follow the [coding-guidelines](#guidelines).
- Give your pull request a helpful title that summarizes what your contribution does.
- Link your pull request to the issue (see:
  [closing keywords](https://docs.github.com/en/github/managing-your-work-on-github/linking-a-pull-request-to-an-issue)
  for an easy way of linking your issue)
- All public methods should have informative docstrings with sample usage presented as doctests when appropriate.
- At least one paragraph of narrative documentation with links to references in the literature (with PDF links when
  possible) and the example.
- If your feature is complex enough that a doctest is insufficient to fully showcase the utility, consider creating a
  Jupyter notebook to illustrate use instead
- All functions and classes must have unit tests. These should include, at the very least, type checking and ensuring
  correct computation/outputs.
- All code should be automatically formatted by `black`. You can run this formatter by calling:

  ```sh
  pip install black
  black path/to/your_module.py
  ```

- Ensure all tests are passing locally using `pytest`. Install the necessary
  packages by:

  ```sh
  pip install pytest pytest-cov
  pytest
  ```

- If you are proposing adding a new module, make sure you are inheriting from the appropriate base class. See
  [the documentation](https://hyppo.neurodata.io/api/index.html#base-classes) for the appropriate class.

### All Contributors Bot

For all your hard work, please add yourself using the All Contributors bot. Follow instruction [here](https://allcontributors.org/docs/en/bot/usage).

## Guidelines

### Coding Guidelines

Idiomatic code enables us to easily share ownership and faster modification of code. Hyppo package closely follows the official
Python guidelines as detailed in [PEP8](https://www.python.org/dev/peps/pep-0008/), it provides the exact details on how code the should be formatted and indented in a python file. Please read it and follow it's guidelines while contributing.

### Docstring Guidelines

The hyppo package closely follows the numpydoc guidelines. Proper formatting of docstrings is essential to generate documentation by Sphinx. Please go through the [numpydoc](https://numpydoc.readthedocs.io/en/latest/format.html#overview) and follow it's guidelines. Also, Refer to the [example.py](https://numpydoc.readthedocs.io/en/latest/example.html#example) provided by numpydoc.

### Commit and Pull Request Naming Conventions
When making commits and pull requests, please follow these best practices:

#### Commit Naming Conventions

- Start with a concise summary: Begin the commit message with a short, descriptive summary of the changes made in the commit. Limit the subject line to 50 characters and provide a detailed description in the body of the commit. Keep it brief but meaningful.
- Use present tense: Write the commit message using present tense, as if you're describing the current state of the codebase after applying the changes.
- Use imperative mood: Formulate the summary in an imperative mood, which means starting with a verb. For example, use "Add feature," "Fix bug," or "Update documentation."
- Provide additional details: If needed, include additional information in the commit message, such as motivation, context, or any relevant issue or pull request references. It helps others understand the rationale behind the changes.

#### Pull Request Naming Conventions

- Start with a clear prefix: Begin the pull request (PR) title with a clear prefix that indicates its purpose. Common prefixes include "Feature:", "Bug Fix:", "Documentation:", or "Refactor:".
- Use a descriptive summary: Provide a concise but descriptive summary of the changes introduced by the PR. This will provide reviewers with a quick understanding of what the PR aims to accomplish.
- Include issue references: If the PR addresses a specific issue or feature request, it's helpful to include the corresponding issue number or link in the PR title. This helps track the relationship between the PR and the underlying task.


- For more information on commit message best practices, you can refer to the documentation of [scipy](https://pypi.org/project/Scripy/) or [scikit-learn](https://scikit-learn.org/stable/). 
