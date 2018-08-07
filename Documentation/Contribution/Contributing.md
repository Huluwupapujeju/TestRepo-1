---
layout: model
title: Deep Convolutional Generative Adversarial Network
tags: [ tag-a, tag-b ]
---

VergeML Contributing Guide
============

Hi! I’m really excited that you are interested in contributing to Vue.js. Before submitting your contribution though, please make sure to take a moment and read through the following guidelines.

   * Code of Conduct
   * Issue Reporting Guidelines
   * Pull Request Guidelines
   * Development Setup
   * Project Structure


Pull Request Guidelines
============

   * The `master` branch is basically just a snapshot of the latest stable release. All development should be done in dedicated branches. **Do not submit PRs against the `master` branch.**

   * Checkout a topic branch from the relevant branch, e.g. `dev`, and merge back against that branch.

   * Work in the `src` folder and DO NOT checkin `dist` in the commits.

   * It's OK to have multiple small commits as you work on the PR - we will let GitHub automatically squash it before merging.

   * Make sure `npm test` passes. (see development setup)

   * If adding new feature:

        * Add accompanying test case.
        * Provide convincing reason to add this feature. Ideally you should open a suggestion issue first and have it greenlighted before working on it.

   * If fixing a bug:

        * If you are resolving a special issue, add `(fix #xxxx[,#xxx])` (#xxxx is the issue id) in your PR title for a better release log, e.g. `update entities encoding/decoding (fix #3899)`.
        * Provide detailed description of the bug in the PR. Live demo preferred.
        * Add appropriate test coverage if applicable.

Development Setup
============

You will need Python version 3.6 and Java Runtime Environment (needed for running Selenium server during e2e tests).

After cloning the repo, run:

$ npm install 