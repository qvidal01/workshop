# Support

Thank you for using the OpenFaaS Workshop! This document provides guidance on how to get help.

## Getting Help

### Workshop-Specific Questions

If you have questions about this workshop or encounter issues while completing the labs:

1. **Check the Documentation**
   - Review the specific lab instructions carefully
   - Check the [Appendix](./appendix.md) for additional information
   - Review the [README](./README.md) for prerequisites and setup

2. **Search Existing Issues**
   - Search [existing GitHub issues](https://github.com/openfaas/openfaas-workshop/issues) to see if your question has been answered
   - Check closed issues as well - many common problems have been solved

3. **Create a New Issue**
   - If you can't find an answer, [create a new issue](https://github.com/openfaas/openfaas-workshop/issues/new)
   - Use the issue template and provide:
     - Which lab you're working on
     - What you expected to happen
     - What actually happened
     - Your environment details (OS, Kubernetes version, etc.)
     - Steps to reproduce the problem

### OpenFaaS General Questions

For questions about OpenFaaS itself (not workshop-specific):

1. **Official Documentation**
   - Visit [docs.openfaas.com](https://docs.openfaas.com)
   - Check the [FAQ](https://docs.openfaas.com/deployment/troubleshooting/)

2. **OpenFaaS Community Slack**
   - Join the community at [slack.openfaas.io](https://slack.openfaas.io)
   - Ask questions in the `#general` or `#kubernetes` channels
   - Be respectful and follow the [Code of Conduct](./CODE_OF_CONDUCT.md)

3. **OpenFaaS GitHub Repositories**
   - [openfaas/faas](https://github.com/openfaas/faas) - Core project
   - [openfaas/faas-cli](https://github.com/openfaas/faas-cli) - CLI tool
   - [openfaas/faas-netes](https://github.com/openfaas/faas-netes) - Kubernetes provider

### Updated Learning Materials

As noted in the README, this workshop was created in 2017/2018. For the most current materials:

- [Complete handbook with JavaScript](https://gumroad.com/l/serverless-for-everyone-else)
- [Serverless on Kubernetes Course by the LinuxFoundation](https://www.openfaas.com/blog/introduction-to-serverless-linuxfoundation/)

## Common Issues

### Installation Problems

**Issue**: Can't install OpenFaaS CLI
- **Solution**: Follow the [latest installation guide](https://docs.openfaas.com/cli/install/)
- Check you have the correct permissions (sudo on Linux/Mac)

**Issue**: Kubernetes cluster not starting
- **Solution**: Ensure Docker is running and has enough resources (4GB RAM minimum)
- Try restarting Docker Desktop
- For k3d, try `k3d cluster delete` and recreate

### Deployment Problems

**Issue**: Functions won't deploy
- **Solution**: Verify `OPENFAAS_PREFIX` is set correctly
- Check you're logged into Docker Hub: `docker login`
- Verify OpenFaaS is running: `kubectl get pods -n openfaas`

**Issue**: Can't access OpenFaaS gateway
- **Solution**: Check port-forward is running: `kubectl port-forward -n openfaas svc/gateway 8080:8080`
- Verify `OPENFAAS_URL` is set: `echo $OPENFAAS_URL`

### Build Problems

**Issue**: Function build fails
- **Solution**: Check the function handler syntax
- Verify `requirements.txt` dependencies are correct
- Check Docker daemon is running

## Contributing

Found a bug or want to improve the workshop?

- Read the [Contributing Guide](./CONTRIBUTING.md)
- Review the [Code of Conduct](./CODE_OF_CONDUCT.md)
- Submit a pull request with your improvements

## Professional Support

### OpenFaaS Support

OpenFaaS offers professional support for teams and enterprises:

- Visit [openfaas.com](https://www.openfaas.com/) for details
- Commercial support includes:
  - Architecture review
  - Training
  - Custom development
  - Priority support

### Sponsorship

OpenFaaS is an independent open source project. Consider sponsoring:

- [GitHub Sponsors for OpenFaaS](https://github.com/sponsors/openfaas)

Your support helps maintain and improve the project.

## Resources

### Official Links

- [OpenFaaS Website](https://www.openfaas.com/)
- [OpenFaaS Documentation](https://docs.openfaas.com/)
- [OpenFaaS Blog](https://www.openfaas.com/blog/)
- [OpenFaaS YouTube Channel](https://www.youtube.com/c/OpenFaaS)

### Community

- [OpenFaaS Slack](https://slack.openfaas.io)
- [OpenFaaS Twitter](https://twitter.com/openfaas)
- [Community Page](https://github.com/openfaas/faas/blob/master/community.md)

### Learning Resources

- [Serverless For Everyone Else](https://gumroad.com/l/serverless-for-everyone-else)
- [OpenFaaS Blog Tutorials](https://www.openfaas.com/blog/)
- [Community Blog Posts](https://github.com/openfaas/faas/blob/master/community.md)

## Response Times

This is a community-driven project. Response times vary:

- **GitHub Issues**: Usually reviewed within 1-3 business days
- **Slack**: Real-time community support during business hours (volunteers)
- **Pull Requests**: Reviewed within 1 week for well-documented changes

For urgent or time-sensitive issues, consider professional support.

## Feedback

We value your feedback! Let us know:

- What worked well
- What was confusing
- Ideas for improvement
- Success stories

Open an issue or reach out on Slack. Thank you for being part of the OpenFaaS community!

---

**Last Updated**: 2025-11-17
