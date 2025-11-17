# Security Policy

## Supported Versions

This workshop project is educational in nature. While we strive to keep dependencies up to date, please note:

| Version | Supported          | Notes                                    |
| ------- | ------------------ | ---------------------------------------- |
| Latest  | :white_check_mark: | All security updates applied             |
| Older   | :x:                | Please use the latest version            |

## Reporting a Vulnerability

We take security seriously. If you discover a security vulnerability in this workshop or any of the example code, please report it to us privately.

### How to Report

1. **Do NOT** create a public GitHub issue for security vulnerabilities
2. Report security issues to the OpenFaaS project maintainers via:
   - The OpenFaaS Slack community (join at https://slack.openfaas.io)
   - Email the project maintainers directly
   - Use GitHub's private vulnerability reporting feature

### What to Include

When reporting a vulnerability, please include:

- Description of the vulnerability
- Steps to reproduce the issue
- Potential impact
- Suggested fix (if available)
- Your contact information for follow-up

### What to Expect

- **Acknowledgment**: We will acknowledge receipt of your vulnerability report within 48 hours
- **Assessment**: We will assess the vulnerability and determine its severity
- **Fix Timeline**: We will work to fix confirmed vulnerabilities as quickly as possible
- **Disclosure**: Once a fix is available, we will:
  - Release a security update
  - Credit you for the discovery (unless you prefer to remain anonymous)
  - Publish details in a security advisory

## Security Best Practices

When using this workshop, please follow these security best practices:

### Dependencies

- Always use the latest versions of dependencies
- Regularly update Python packages using `pip install --upgrade`
- Review the `requirements.txt` files for pinned versions
- Use Dependabot alerts (enabled in this repository)

### Secrets Management

- **NEVER** commit secrets, API keys, or passwords to version control
- Use Kubernetes secrets as demonstrated in Lab 10
- Use environment variables for sensitive configuration
- Review `.gitignore` to ensure secrets are excluded

### Docker Images

- Use official base images from trusted sources
- Regularly update base images to get security patches
- Scan images for vulnerabilities using tools like:
  - `docker scan`
  - Trivy
  - Snyk

### OpenFaaS Deployment

- Enable authentication on the OpenFaaS gateway
- Use TLS/HTTPS in production (see Lab documentation)
- Implement HMAC validation for webhooks (see Lab 11)
- Use read-only filesystems where possible (see Lab 4)
- Follow the principle of least privilege

### Code Security

- Validate all user input
- Avoid using `eval()` or similar dynamic code execution
- Use parameterized queries for database access
- Implement rate limiting on functions
- Review CodeQL alerts in this repository

## Known Security Considerations

### Workshop Environment

This workshop is designed for **learning purposes only**. The example code:

- Uses simplified authentication for demonstration
- May not implement all production security best practices
- Should be reviewed and hardened before production use

### Example Functions

The example functions in this workshop:

- `hello-openfaas`: Basic example with no security concerns
- `astronaut-finder`: Makes external HTTP requests (ensure trusted sources)
- `issue-bot`: Handles GitHub webhooks (implement HMAC validation)
- `hmac-protected`: Demonstrates webhook security

## Resources

- [OpenFaaS Security Documentation](https://docs.openfaas.com/architecture/authentication/)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [Kubernetes Security Best Practices](https://kubernetes.io/docs/concepts/security/)
- [Python Security Best Practices](https://python.readthedocs.io/en/stable/library/security_warnings.html)

## Automated Security

This repository includes automated security scanning:

- **CodeQL**: Scans for security vulnerabilities in code
- **Dependabot**: Monitors dependencies for known vulnerabilities
- **Bandit**: Python security linter
- **Pre-commit hooks**: Detect secrets and security issues

Please review and address any security alerts promptly.

## Updates

This security policy was last updated: 2025-11-17

For questions about this policy, please open an issue or contact the maintainers.
