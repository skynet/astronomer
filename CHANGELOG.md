# Changelog

All notable changes to this project will be documented in this file.

## [0.0.27] - 2018-02-04

### Changed

- Bump commander and phoenix. Adds support for private docker registry.

## [0.0.23] - 2018-02-03

### Added

- Entrypoint script for docker registry.

## [0.0.22] - 2018-02-03

### Added

- Module/Component labels.

### Changed
- Fixed phoenix image.

## [0.0.19] - 2018-02-02

### Added

- Registry.

## [0.0.18] - 2018-02-01

### Added

- Commander.
- Phoenix.

## [0.0.17] - 2018-01-26

### Added

- Labels for open.

## [0.0.16] - 2018-01-12

### Changed

- Airflow worker-gc environment variable name.

## [0.0.15] - 2018-01-10

### Added

- Support for clearing worker logs after x days.

### Removed

- Snakebite python package due to compatibility issues with python 3.

## [0.0.14] - 2018-01-08

### Changed

- Fixed busted grafana build.

## [0.0.13] - 2018-01-07

### Added

- Support for passing default prometheus host for grafana datasource.

## [0.0.12] - 2018-01-07

### Changed

- Prometheus config file name and paths.

## [0.0.11] - 2018-01-05

### Added

- Prometheus Marathon config.

## [0.0.10] - 2018-01-04

### Added

- Python and pip symlinks to python3 and pip3.

### Removed

- Usage of .astro directory in start script.

## [0.0.9] - 2018-01-04

### Added

- Vendor images.

## [0.0.8] - 2018-01-03

### Added

- Tini init system.

## [0.0.5] - 2017-12-15

### Added

- Support for Airflow onbuild tags.

## [0.0.4] - 2017-12-15

### Added

- This Changelog
- StatsD package to Airflow
- StatsD exporter to stack.
- Prometheus to stack.
- Grafana to stack.

### Changed

- Airflow scripts now run docker-compose with -d flag.
