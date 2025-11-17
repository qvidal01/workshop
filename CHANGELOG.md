# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- GitHub Actions workflows for CI/CD automation
  - Link checker for documentation
  - Markdown linting
  - Python code linting and security scanning
  - YAML validation
  - Spell checking
- Dependabot configuration for automated dependency updates
- CodeQL security scanning workflow
- Pre-commit hooks configuration for local development
- Community health files (CODE_OF_CONDUCT.md, SECURITY.md, SUPPORT.md)
- .editorconfig for consistent code formatting
- pyproject.toml for Python tooling configuration
- Enhanced deprecation notice with version compatibility matrix

### Changed
- Pinned Python dependencies to specific versions for reproducibility
  - requests==2.31.0
  - PyGithub==2.1.1
- Enhanced README with prominent workshop status notice
- Improved .gitignore with Python and development patterns

### Security
- Added automated security scanning with CodeQL
- Added Bandit security linter for Python code
- Pinned dependencies to specific versions to prevent supply chain attacks

## [Historical Changes]

### 2024-01-15
- Update Japanese instructions for markdown file
- Update instruction for deploying markdown function
- Update lab1b.md
- Update address for arkade
- Fix broken GH sponsor link in README

### 2023-12-10
- Update GH Sponsors tagline
- Remove uname from markdown examples
- Update Lab11 to be more reflective of code

### 2023-11-05
- Fix issue with auth_token variable in quotes
- Update note on bash for MacOS
- Fix broken image links in Japanese translated Lab 5
- Fix link to Lab 5 from Lab 11

### 2023-10-01
- Update default gateway to gateway.openfaas
- Fix filename reference
- Convert from broken Ngrok to inlets

---

## Notes

For a complete history of changes, please refer to the [commit history](https://github.com/openfaas/openfaas-workshop/commits/).

### Categories

- `Added` for new features
- `Changed` for changes in existing functionality
- `Deprecated` for soon-to-be removed features
- `Removed` for now removed features
- `Fixed` for any bug fixes
- `Security` for vulnerability fixes
