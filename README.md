# Unity WebGL: Automatic build and gh-pages deployment

```mermaid
journey
	title WebGL Automatic Build and Deployment
	section Prepare files for deployment
        Git LFS Sample:6: Unity Build
		Stash and Restore:6: Unity Build
		Clean Target: 6: Unity Build
        Apply Stash: 6: Unity Build
        Relocate Files: 6: Unity Build
        Push: 6: Unity Build
    section GH Pages Deployment
        Deploy: 6: Pages
```

```mermaid
---
title: Git workflow
---
gitGraph
   commit
   branch 18-ci-cleaning-deployment-branch
   checkout 18-ci-cleaning-deployment-branch
   commit
   commit
   checkout main
   merge 18-ci-cleaning-deployment-branch
   checkout gh-pages
   commit
```

This repository contains a Unity WebGL project that is automatically built by using Github Actions and following certain rules.

Based on [GameCI](https://game.ci/docs/github/getting-started/)

## SUPPORT
- Git LFS

- **Platforms**
	- WebGL (**Not compressed builds**).

## REQUIREMENTS

### Acquire Activation File
[GameCI Documentation](https://game.ci/docs/github/activation).


## OUTPUT

### Artifact
Downloadable zip with the build files.

### Automatic deployment to Github Pages
Build content is deployed to the target branch, where Github pages should be pointing to.

## CONFIGURABLE

It is based on the use of repo enviroment variables:

- TARGET_PLATFORM
- BUILD_PATH
- ARTIFACT_NAME
- DEPLOYMENT_BRANCH

