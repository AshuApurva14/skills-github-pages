## Using GitHub Actions on Pull Request

**Setting up GitHub Actions on Pull Requests**

1. Getting started with a workflow file:
   - Workflows are defined under the `.github/workflows` directory in the repository. These are written in YAML format.
   - To create a workflow that triggers on pull request events, you start by defining the name and the event that triggers the workflow in a YAML file.
   - Below are the example:


   ```bash
   # Example Workflow to define PR based Trigger
   
    name: Example PR Workflow
    on:
      pull_request:
        types: [opened, synchronize, reopened, closed]
    
    jobs:
      build:
        runs-on: ubuntu-latest
        steps:
          - uses: actions/checkout@v3
          - name: Run a one-line script
            run: echo "The event type is ${{ github.event.action }}"

   ```
