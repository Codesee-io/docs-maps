# Pull Request Maps

Once [a map is installed on a repository](./installation.md), pull request maps will be automatically generated for them.

## Generating a pull request map

Might sound straightforward, and that's because it is! All you have to do is create a pull request on your repo.

Once that's done, the `codesee-architecture-diagrams` bot will automatically comment on your pull request with an image of a map, along with a legend showing how these have changed. Below is an example from [Distribute Aid](https://distributeaid.org/)'s public repository:

![Generated diagram showing a pull request](img/pr-map.svg)
![Generated CodeSee map legend](img/pr-map-legend.png)

The legend consists of three types of changes:

- **Added**: Files/folders added in this pull request
- **Removed**: Files/folders removed in this pull request
- **Edited**: Files/folders that have been modified in this pull request

If commits are made to this pull request, a new PR diagram will be generated.