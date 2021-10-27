# Review Maps

Once [a map is installed on a repository](./installation.md), Review Maps will be automatically generated for every pull request made to the repository. There is also an “Install Review Maps” button on the /maps page which will get you up-and-running. 

## Generating A Review Map

To get started, make a pull request to the repository.

Once that's done, the `codesee-architecture-diagrams` bot will automatically comment on your pull request with an image of a Map showing the files impacted by the PR, along with a Map legend. Below is an example from [Distribute Aid](https://distributeaid.org/)'s public repository:

![Generated diagram showing a pull request](img/pr-map.svg)
![Generated CodeSee map legend](img/pr-map-legend.png)

The legend consists of three types of changes:

* **Added**: Files/folders added in this pull request
* **Removed**: Files/folders removed in this pull request
* **Edited**: Files/folders that have been modified in this pull request

If commits are made to this pull request, a new Review Map will be generated.

## Review Map Capabilites 

* **Side-by-side code comparison**: Double-click on individual files in a Map to view code in a side-by-side diff.
* **Intuitive grouping**: Code is grouped intuitively so that you can review based on logic and functionality. For example, you can choose to review left to right (general to more specific) or vice versa and review sections based on type (back-end vs. front-end changes, etc.).
* **Add Comments**: Provide feedback on code reviews by placing and responding to Comments—they're automatically reflected in the GitHub repository.
* **Progress Bar** : Easily mark sections as 'Reviewed' as you move through a code review.
