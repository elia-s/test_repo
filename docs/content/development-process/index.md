---
date: 2016-03-09T19:56:50+01:00
title: Development Process
weight: 20
---

## Code Versioning and Working Practice
- The code of the MIP is versioned into Github.
- Each project should contain at least a master branch and a stable branch.
- The stable branch should contain only strongly tested code that can be used in a production environment.
- The master branch should contain the latest working features that needs to be strongly tested before being merged to the stable branch.
- Each developer should create new branches (usually from the master branch) to implement new features and/or to fix bugs.
- No one should directly commit changes into the stable or master branch. Once feature/bug-fix branch is working the branch can be merged into the master one.
- For big changes, a merge request should be created and assigned to another developer.
- AUTOMATION: The stable branch should never be updated manually. The CI system should look for changes in the master branch and automatically run some tests on it. If the automatic tests are successfully passed, the CI system will create a merge request from the master branch to the stable branch or automatically do the merge.

## Testing (Unit and Integration)
1. Each component should include unit tests which should be executed each time will build it.
2. Each built component (usually a Docker image) should also be tested with integration tests before being pushed on a repository (usually Docker Hub). These tests are needed by the CI system to decide whether a feature can be considered stable enough for the stable branch.

## Docker Images Versioning
As Docker is a key technology in our platform, each Docker component we build should be versioned using a "Git commit hash" and pushed on [Docker Hub](https://hub.docker.com/u/hbpmip/) or on our private Docker Registry server. In this way, we will always be able to retrieve the precise code (on GitLab) that was used to build an Docker image.

We will also be able to rollback or commit a new version of a component in a very easy way.

##Binaries Versioning
As a few components like libraries should be built for "non-docker" use. These will be versioned and pushed on Artifactory.
