# Build Flow.yaml

This GitHub Actions workflow, ****Build Flow****, automates the build and deployment process for our project. It runs on every push to any branch, performing the following steps:  <br />

**Setup:** Checks out the repository and sets up Node.js (v16).  <br />
**AWS Authentication:** Configures AWS credentials using a workload identity provider for secure access.  <br />
**Private Module Access:** Configures access to private Git and NPM modules.  <br />
**Caching and Installation:** Restores node_modules cache and installs dependencies.  <br />
**Build & Deployment:** Builds the project and deploys it to the production and staging environments on AWS.  <br />

This workflow enables continuous deployment with each code push, ensuring the latest changes are always live.  <br />

# Create PR to Master.yaml

This GitHub Actions workflow, **Create PR to Master**, allows for easy creation of pull requests (PRs) from the development branch to the master branch. It can be manually triggered with a workflow dispatch event, accepting a required PR title and an optional ticket number as inputs. <br />

**Check Existing PRs:** Verifies if an open PR from development to master already exists.  <br />
**Create New PR:** If no existing PR is found, it creates a new PR with a title prefixed by the ticket number and "PROD RELEASE."  <br />
**Fail if Duplicate:** If an open PR already exists, the workflow stops with an error message, linking to the existing PR.  <br />

This workflow standardizes PR creation for production releases and prevents duplicate PRs to master.  <br />
