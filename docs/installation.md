# Installation

To get started using CodeSee Maps, you will need to authorize CodeSee on your GitHub user account, then install and authorize the CodeSee Architecture Diagrams GitHub action on the repositories you’d like to create maps for.

## Installing CodeSee Maps
1. Go to [https://app.codesee.io/maps](https://app.codesee.io/maps) to sign in.
1. Select “Connect to GitHub,” then “Authorize Codesee-io” to add CodeSee to your account.
1. Click “+ New Codebase Map”
1. If you are the first person in your GitHub organization to create a Map, you will need to install the GitHub action.
    1. Click “Install” then choose the appropriate organization.
    1. Click “Install & Authorize.”
1. Select the repository you’d like to create a diagram of and click “Continue.”
1. Follow the instructions to add the CodeSee API token to your repo’s secrets page, then click “Create Map Diagram.”
1. Your map should be ready to explore, annotate, and share!

### Updating the CodeSee API Token
1. Go to your repo’s Secrets page.
1. Click the “Update” button.
1. Copy the API token, paste it into the form, then click the “Update Secret” button.

## Listing Your Map in Your Documentation

We provide a badge for you to use in your documentation:
![View Architecture Diagram badge for CodeSee](https://codesee-docs.s3.amazonaws.com/badge.svg)

You can include this in your documentation, such as your README.md file, with the following markdown example:

```
[![View Architecture Diagram badge for CodeSee](https://codesee-docs.s3.amazonaws.com/badge.svg)](YOUR_CODESEE_MAP_URL)
```

## Permissions

We currently request the following GitHub permissions to ensure that you have an amazing experience using CodeSee

### Access to Content and Workflows

We currently run our Maps analysis using a GitHub action (though more options are on the way). Your code is analyzed on GitHub's servers -- we do not store it! Our action sends us aggregate data and metadata about your codebase and then we use that to create your map, to make insights, and more. In addition, these permissions enable us to open PRs (dependabot style) to install and update the CodeSee Map workflow in your repo to the latest configuration. Finally, if you use our Code Review Maps feature, we display code changes in our UI alongside a Map of the pull request. We do so by requesting only the relevant code using GitHub's APIs, and transmitting it securely over https. Again, we do not store your code.

### Access to Pull requests

For pull requests, we post a PR Map on each of your pull requests so that you can see how your change fits within the larger architecture. We need your permission to make that possible.

### Access to Actions

These allow us to monitor our GitHub Action, to present progress indicators in app, and help you troubleshoot if and when something goes wrong. 

### Access to Repo Administration Organization Members

We use information about who has access to your repo and organization in order to limit who has access to your CodeSee Maps. That way, all those and only those who have access to your repo will have access to your Maps about that repo. 
