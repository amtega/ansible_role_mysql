# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
## [1.4.4] - 2022-04-22
### Changed
- Add innodb-print-all-deadlocks to my.cnf. Related ansible/playbooks/mysql#19

## [1.4.3] - 2022-04-20
### Fixed
- Fixes a bug that caused the installation to fail when using 3 digits in the version. Related ansible/playbooks/mysql#20

## [1.4.2] - 2022-04-07
### Fixed
- Adjust log directory selinux context. Related to ansible/roles/amtega.mysql/-/issues/9

## [1.4.1] - 2022-02-22
### Fixed
- Adapted for CentOS derived distros. Related to ansible/main#263

## [1.4.0] - 2022-02-16
### Changed
- Adapted for CentOS derived distros. Related to ansible/main#263

## [1.3.0] - 2022-02-02
### Changed
- Supported distros. Related to ansible/main#178
