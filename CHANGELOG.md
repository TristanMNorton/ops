# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.8.0] - 2018-09-19

### Removed
- PHP Version URLs. Use `OPS_PROJECT_BACKEND` dotenv var
- `OPS_PROJECT_PHP_VERSION` dotenv var
- Custom self signed cert generator

### Added
- "Remote" mode with Let's Encypt DNS challenge support
- nginx/openresty proxy for reading dotenv
- `OPS_DEFAULT_DOCROOT` global config option
- `OPS_DEFAULT_BACKEND` global config option
- `OPS_ADMIN_AUTH` global config option for remote mode
- `OPS_PROJECT_BACKEND` project config option
- `OPS_PROJECT_DOCROOT` project config option
- `OPS_PROJECT_BASIC_AUTH` project config option
- `OPS_PROJECT_BASIC_AUTH_FILE` project config option
- Version tracking through ~/.ops/VERSION file

### Fixed
- `mariadb import` and `psql import` STDIN handling
- Big refactor of script variables
- `ops sync` db vars now optional (host, name, port, pass)

## [0.7.5] - 2018-08-30

### Added
- php 5.6: Added php zip extension and webgrind

## [0.7.4] - 2018-08-23

### Added
- **dashboard** Proper php links for 5.6, 7.1, and 7.2

## [0.7.3] - 2018-08-23

### Fixed
- **dashboard** fixed php NOTICE

## [0.7.2] - 2018-08-15

### Added
- Lots of php 5.6 extensions

### Fixed
- `psql import` IF EXISTS clause

### Changed
- php `upload_max_filesize` and `post_max_size` are now 100M
- php `display_errors` and `display_startup_errors` are now on

## [0.7.1] - 2018-08-14

### Fixed
- **dashboard** project links respect custom php version
- `ops shell` respects custom php version

## [0.7.0] - 2018-08-13

### Added
- php image dockerfiles moved to ops repo
- official ops docker images: imarcagenct/ops-apache-php*
- php 5.6 support
- php 7.2 support

## [0.6.1] - 2018-08-03

### Fixed
- `psql import` now works properly
- `OPS_PROJECT_REMOTE_DB_HOST` fixed for mariadb/mysql

### Added
- `OPS_PROJECT_REMOTE_DB_PASSWORD` added for mariadb/mysql
- `OPS_PROJECT_REMOTE_DB_PORT` added for mariadb/mysql

## [0.6.0] - 2018-06-22

### Added
- **dashboard** tooltip for 'live' project badge
- `ops sync` command
- `ops system refresh-certs` command
- `ops system refresh-config` command
- `ops system refresh-services` command
- `ops mariadb create` command
- `ops psql create` command

### Changed
- `ops psql` is now `ops psql cli`
- `ops psql-import` is now `ops psql import`
- `ops psql-export` is now `ops psql export`
- `ops mariadb` is now `ops mariadb cli`
- `ops mariadb-import` is now `ops mariadb import`
- `ops mariadb-export` is now `ops mariadb export`

## [0.5.0] - 2018-05-24

### Added
- Changelog!

### Changed
- `ops shell` now runs bash as www-data within the running container
