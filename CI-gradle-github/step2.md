# What is GitHub Actions?
GitHub actions is a platform that allows you to automate your builds, tests and deployment through pipelines for Continuous Integration and Delivery (CI/CD). GitHub actions allows you to setup workflows such as running tests or build when new pull requests are made. You can also run workflows when other events are made in the repository.

# Workflows
A workflow is something that is triggered when an event occurs in your repository. It could be to run all tests on the event that a new pull request is made. A workflow consists of jobs which will be run sequentally or in parallell inside a container. A job could be to run certain scripts or actions. Workflows are configured by a YAML file located in your repository and will run when triggered by an event, or manually but can also be set to run defined by a schedule. Actions are custom applications for the GitHub Actions platform which performs some frequently repeated task. An example of an action could be to pull your repository and setup the correct tools for your build enviroment.

Later on in this tutorial in step 5 we will create an YAML file for CI with GitHub actions.
