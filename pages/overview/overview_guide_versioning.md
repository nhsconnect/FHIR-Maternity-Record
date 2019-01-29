---
title: Guide Versioning
keywords: development, versioning
tags: [development]
sidebar: overview_sidebar
permalink: overview_guide_versioning.html
summary: An overview of this implementation guide is versioned.
---

## Beta ##

This implementation guidance is the **Beta** release to support the development of the Digital Child Health (TEST) Event Messages. 

## Semantic Versioning ##

Given a version number MAJOR.MINOR.PATCH, increment the:

- MAJOR version when you make incompatible API changes,
- MINOR version when you add functionality in a backwards-compatible manner, and
- PATCH version when you make backwards-compatible bug fixes.

Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

A pre-release version MAY be denoted by appending a hyphen (refer to [Semantic Versioning - Item 9](http://semver.org/#spec-item-9){:target="_blank"})

For examples: 1.0.0-alpha.1 is a valid pre-release version.

## Pre-release Labels ##

These labels will be taken from the GDS development process stages, and will be one of:

 - **Experimental**: Early development/POC version of an API for early sight during discovery
 - **Alpha**: Initial test APIs, likely to change substantially, or be discontinued as the project develops
 - **Beta**: APIs that are still under active development and subject to change, but that are likely to progress into a live API
 - **Release Candidate**: APIs that are largely complete, unlikely to change substantially, but still need further testing before becoming live
 - **Live**: Release live APIs
 - **Discontinued**: APIs which have been discontinued and should not be used for new development.


