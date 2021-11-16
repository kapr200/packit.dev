---
title: "November 2021"
date: 2021-11-08
draft: false
weight: 69
---

## Week 44 (November 1st - November 5th)

- We have fixed several issues in packit when it's periodically checking
  statuses of jobs. You should now reliably see up to date check statuses for
  Copr RPM builds and Testing Farm runs.
  ([packit-service#1267](https://github.com/packit/packit-service/pull/1267)),
  ([packit-service#1265](https://github.com/packit/packit-service/pull/1265))
- Fixed an issue, which raised a `UnicodeEncodingError`, when working with
  dist-git patch files with an encoding other than UTF-8.
  ([packit#1406](https://github.com/packit/packit/pull/1406))
- Backup alias definitions now reflect the official release of Fedora 35.
  ([packit#1405](https://github.com/packit/packit/pull/1405))

## Week 45 (November 8th - November 12th)

- You can now specify `skip_build` option in the test job metadata in the
  Packit configuration file. This will cause no Copr build to be built and
  installed into the testing environment, but only trigger the tests in
  Testing Farm (the selected components to be installed should be part of the
  TMT definitions).
  ([packit-service#1256](https://github.com/packit/packit-service/pull/1256))
- Packit supports `changelog-entry` action that is used when creating SRPM.
  The action is supposed to generate whole changelog entry (including `- ` at
  the start of the lines) and has a priority over any other way we modify the
  changelog with. ([packit#1367](https://github.com/packit/packit/pull/1367))