# Installation

To get started using CodeSee Maps, you will need to authorize CodeSee on your GitHub user account, then install and authorize the CodeSee Architecture Diagrams GitHub action on the repositories you’d like to create maps for.

## Installing CodeSee Maps
1. Go to [https://app.codesee.io/maps](https://app.codesee.io/maps) to sign in.
1. Select “Connect to GitHub,” then “Authorize Codesee-io” to add CodeSee to your account.
1. Click “Add a new map.”
1. If you are the first person in your GitHub organization to create a map, you will need to install the GitHub action.
    1. Click “Install” then choose the appropriate organization.
    1. Click “Install & Authorize.”
1. Select the repository you’d like to create a diagram of and click “Continue.”
1. Follow the instructions to add the CodeSee API token to your repo’s secrets page, then click “Create Map Diagram.”
1. Your map should be ready to explore, annotate, and share!

### Updating the CodeSee API Token
1. Go to your repo’s secrets page.
1. Click the “Update” button.
1. Copy the API token, paste it into the form, then click the “Update Secret” button.

## Permissions

We currently request the following GitHub permissions to ensure that you have an amazing experience using CodeSee

### Access to code

We currently run our Maps analysis using a GitHub action (though more options are on the way). Your code stays on GitHub's servers, we do not transmit or store it! Our action sends us aggregate data and metadata about your codebase and then we use that to create your map, make insights etc. These permissions enable us to open PRs (dependabot style) to update our workflow to the latest CodeSee Map configuration. 

### Access to Pull requests

For pull requests, we post a PR Map on each of your pull requests so that you can see how your change fits within the larger architecture. We need your permission to make that possible.

### Access to Actions and Workflows

These allow us to monitor our GitHub Action, to present progress indicators in app, and help you troubleshoot if and when something goes wrong. 
