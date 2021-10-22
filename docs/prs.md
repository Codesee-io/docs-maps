# Review Maps

Once [a map is installed on a repository](./installation.md), Review Maps will be automatically generated for every pull request made to the repository. 

## Generating A Review Map

To get started, make a pull request to the repository.

Once that's done, the `codesee-architecture-diagrams` bot will automatically comment on your pull request with an image of a Map showing the files impacted by the PR, along with a Map legend. Below is an example from [Distribute Aid](https://distributeaid.org/)'s public repository:

![Generated diagram showing a pull request](img/pr-map.svg)
![Generated CodeSee map legend](img/pr-map-legend.png)

The legend consists of three types of changes:

- **Added**: Files/folders added in this pull request
- **Removed**: Files/folders removed in this pull request
- **Edited**: Files/folders that have been modified in this pull request

If commits are made to this pull request, a new Review Map will be generated.
