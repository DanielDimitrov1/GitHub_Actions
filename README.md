# GitHub_Actions

# Build Flow.yaml

This GitHub Actions workflow, Build Flow, automates the build and deployment process for our project. It runs on every push to any branch, performing the following steps:  <br />

**Setup:** Checks out the repository and sets up Node.js (v16).  <br />
**AWS Authentication:** Configures AWS credentials using a workload identity provider for secure access.  <br />
**Private Module Access:** Configures access to private Git and NPM modules.  <br />
**Caching and Installation:** Restores node_modules cache and installs dependencies.  <br />
**Build & Deployment:** Builds the project and deploys it to the production and staging environments on AWS.  <br />
This workflow enables continuous deployment with each code push, ensuring the latest changes are always live.  <br />
