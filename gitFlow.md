# The gitFlow workflow

In this document:
* [Why do we need a workflow](#why-do-we-need-a-workflow)
* [Popular GIT workflows](#popular-git-workflows)
* [What is gitFlow](#what-is-gitflow)
* [Key Benefits](#key-benefits)
* [How it works](#how-it-works)
    * [Develop and Master branches](#develop-and-master-branches)
    * [Feature Branches](#feature-branches)
    * [Release Branches](#release-branches)
* [Sources](#sources)
* [Changelog](#changelog)

## Why do we need a workflow?

GIT is designed to be extremely flexible. 
This means that, if left unchecked, each member of a development team will have a different way of managing their code or performing the simplest of tasks, in some cases, this may negate any benefits that a version control system may offer.

GIT workflows are a set of recommendations for how GIT can be used in the most effective way.
To take full advantage of a workflow, it is important for all members of a development team to understand and floow the workflow.

## Popular git workflows

* Centralized
* Feature Branching
* gitFlow
* Forking workflow

it’s important to develop a Git workflow that is a productivity enhancement for your team. In addition to team culture, a workflow should also complement business culture.

## What is gitFlow

* gitFlow is a workflow that helps with continuous software development
* Gitflow is ideally suited for projects that have a scheduled release cycle
* it assigns very specific roles to different branches and defines how and when they should interact. In addition to feature branches, it uses individual branches for preparing, maintaining, and recording releases.


## Key Benefits

* Parallel Development - gitFlow makes parallel development very easy, by isolating new development (such as features and non-emergency bug fixes) from finished work. 

* Collaboration - Feature branches make it easier for two or more developers to collaborate on the same feature, because each feature branch is a sandbox where the only changes are the changes necessary to get the new feature working. That makes it very easy to see and follow what each collaborator is doing.

* Release Staging Area - As new development is completed, it gets merged back into the develop branch, which is a staging area for all completed features that haven’t yet been released. So when the next release is branched off of develop, it will automatically contain all of the new stuff that has been finished.

* Support For Emergency Fixes - GitFlow supports hotfix branches - branches made from a tagged release. You can use these to make an emergency change, safe in the knowledge that the hotfix will only contain your emergency fix. There’s no risk that you’ll accidentally merge in new development at the same time.

## How it works

### Develop and Master branches

* Instead of a single master branch, this workflow uses two branches to record the history of the project. 
* The master branch stores the official release history
* The the develop branch serves as an integration branch for features.
* It's also convenient to tag all commits in the master branch with a version number.

### Feature Branches

* Each new feature should reside in its own branch, which can be pushed to the central repository for backup/collaboration. 
* But, instead of branching off of master, feature branches use develop as their parent branch. When a feature is complete, it gets merged back into develop. 
* Features should never interact directly with master.

### Release Branches

* Once developers has acquired enough features for a release (or a predetermined release date is approaching), you fork a release branch off of develop.
* Creating this branch starts the next release cycle, so no new features can be added after this point — only bug fixes, documentation generation, and other release-oriented tasks should go in this branch.
* Once it's ready to ship, the release branch gets merged into master and tagged with a version number.
* In addition, it should be merged back into develop, which may have progressed since the release was initiated.

* Using a dedicated branch to prepare releases makes it possible for one team to polish the current release while another team continues working on features for the next release.
* It also creates well-defined phases of development (e.g., it's easy to say, “This week we're preparing for version 4.0,” and to actually see it in the structure of the repository).

## Sources

* https://www.atlassian.com/git/tutorials/comparing-workflows
* https://datasift.github.io/gitflow/IntroducingGitFlow.html

## Changelog

* 02/07/2021 - Added gitFlow page
* 02/08/2021 - Added TOC and changelog