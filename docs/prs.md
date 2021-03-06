# Review Maps

Once [a map is installed on a repository](./installation.md), Review Maps will be automatically generated for every pull request made to the repository. There is also an “Install Review Maps” button on the `/maps` page to get you up and running. 

## Generating A Review Map

To get started, make a pull request to the repository.

Once that's done, the `codesee-architecture-diagrams` bot will automatically comment on your pull request with an image of a Review Map showing the files impacted by the PR, along with a Map Legend. Code is grouped intuitively so that you can review based on logic and functionality. For example, choose to review left to right (general to more specific) or review sections based on type (back-end vs. front-end changes, etc.)

![Generated Review Map showing a pull request](img/review-map.png)

The Map Legend consists of three types of changes:

* **Added**: Files/folders added in this pull request
* **Removed**: Files/folders removed in this pull request
* **Edited**: Files/folders that have been modified in this pull request

If commits are made to a pull request, a new Review Map will be generated.

## Interacting With A Review Map

Directly below your Review Map is a link to "Review in an interactive map," allowing you to explore the individual nodes of your Map. Click on a file to highlight its connections. Expand and collapse folders or zoom into and out of the Review Map by using the Zoom UI. 

To access PR-related details during the review, look to the header at the top of the page. Then,

  * Click the PR title or number to navigate to that PR in GitHub.
  * Click the PR author to visit that user’s page in GitHub.
  * Click on the (i) icon to see the full PR description.

### Code Diffs

Double-click on individual nodes in a Map to view code in a diff format. Each file gets a color swatch that indicates whether the file was added, removed, edited, renamed, or is unchanged. 

Double-clicking on an “unchanged” file (the white nodes on the Map) will also display their code.

When viewing a file, any related files (files it imports, and files that import it) that remain unchanged will also be listed in the diff. Unchanged files start with all their code hidden, but can be displayed by clicking on a file header to expand/collapse that file. 

To return to the full Review Map, click on the back arrow in the header. 

### Progress Bar

Mark sections as 'Reviewed' via the checkboxes as you move through the code review. When the checkbox is selected, nodes on the Map are displayed as “Reviewed,” and files within the diff collapse. A progress bar indicating the number of files in the PR that have been reviewed is visible in the header. 

### Comments

Provide feedback on reviews by placing and responding to comments. You can add comments on specific lines within the code diffs or in the pull request discussion within the side panel. Comments are instantly reflected in both the repository and in CodeSee.

![Discussion in a pull request](img/discussion-side-panel.png)

Once a code review conversation is resolved, click "Resolve conversation" to collapse the thread. You can always bring it back by expanding the thread again and clicking on "Unresolve conversation":

<img alt="Resolve a conversation" src="../img/resolve-conversation.gif" width="474">

### Mark files as viewed

When performing a code review, it can be helpful to note files that have undergone review to keep track of progress. When viewing a file diff, click the checkbox on the top right to mark the file as "Reviewed":

![Interact with a Review Map](img/reviewed.gif)

### Review Map Settings

The Review Map settings can be accessed using the menu on the right side:

<img alt="Gif of accessing the Review Map settings" src="../img/review-map-settings.gif" width="306">

By default, all the connections between files and directories are displayed on a Review Map. To reduce visual clutter, turn on the "Hide links between files" setting. In this mode, you can still select files and directories to see the incoming and outgoing connections.

<img alt="Setting to toggle the visibility of links in Review Maps" src="../img/review-map-link-visibility.png" width="256">

The layout of a Review Map is automatically generated. However, we've introduced an experimental flag that allows users to reposition files and directories by dragging them around the page.

<img alt="Setting to toggle the ability to reposition nodes in Review Maps" src="../img/review-map-layout-mode.png" width="256">

## Review Map Tours 

With Review Map Tours, create step-by-step, visual walkthroughs of changes. Pull request authors can offer insight into coding decisions and provide review guidance, like where to begin and how to navigate tricky logic—alerting reviewers on what’s relevant and reducing file switching.

As the **author** of the pull request, you can create a Review Map Tour using comments:

1. Open the CodeSee Review Map linked in your pull request, or log in to Maps, toggle to the Review Maps page, and select a Review Map.
1. Identify what you’d like to communicate to the reviewer. This will help you determine how and where to begin placing the Tour to your code.
1. Double-click the file in your Map where you’d like to begin, opening the code diff. Select a line or section of the code, write your comment, and click 'Add comment', or choose a comment that’s already present. You can use each step of your Tour to offer insight into your coding decisions, provide review tips, and request guidance from the reviewer.
1. To add a comment as a step in your Tour, click the ‘In Tour’ toggle in the lower-right corner of the comment—a new Tour step will appear in the left panel of your interface. 

As the **reviewer** of the pull request, you can view a Review Map Tour to glean additional context about the PR.

1. Open the CodeSee Review Map linked in your pull request, or log in to Maps, toggle to the Review Maps page, and select a Review Map.
1. On the left panel of your interface, shift the toggle from 'Description' to 'Tour' to access the Review Map Tour. 
1. Click 'Start' to begin, and navigate through the 'Next' and 'Previous' buttons to walkthrough the Tour. 
1. Proceed to leave comments as required and complete your review of the pull request.

![Full Review Map Tour experience](img/take-tour-flow.gif)

### Editing Review Map Tours 

As the author of the pull request, you can edit inline, reorder steps in the Tour by clicking and holding the small grid in the upper-right corner of each step, or remove Tour steps by clicking 'Remove from Tour' in the lower-left corner. Your Review Map Tour will automatically save as you work and be visible to anyone who has permission to view the Review Map.

## Submit A Code Review

Click the “Review” button in the header to make a final review comment approving, requesting changes, or commenting on the pull request. 

![Submit review on pull request via a Review Map](img/submit-review.gif)


_A Note On Permissions_: 

On a **public** repository, logged-out users or users without a CodeSee account can view a Review Map. However, users looking to comment or submit a review will be prompted to log in.

On a **private** repository, logged-out users or users without a CodeSee account cannot view a Review Map. The user will be prompted to log in or sign up to view the Review Map.

## Review Maps for Visual Studio Code

CodeSee’s extension for Visual Studio Code allows you to contextualize the potential impact of code changes, address feedback, and submit reviews—all within your editor. 

![CodeSee Review Map on Visual Studio Code](img/codesee-vs-code.gif)

### Install CodeSee for VS Code

> As a prerequisite, ensure you have a [CodeSee account](https://app.codesee.io/) and CodeSee Maps is installed in your repository.

1. You can find the CodeSee Review Maps VS Code extension in the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=codesee.maps). Click **Install** to add the extension to your editor. Alternatively, search for "CodeSee" within VS Code.
2. Install the [GitHub Pull Requests and Issues extension](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github).
3. Open your desired GitHub repository in VS Code.
4. Log in to your CodeSee account when prompted by the sidebar.

### Usage

> Once the CodeSee Review Maps extension is successfully installed, you may begin reviewing all **new** pull requests in VS Code. PRs that predate the extension will not have a Review Map readily available unless a new commit is made.  

#### Local

When browsing a pull request locally, open the command palette with `Ctrl/Cmd` + `Shift` + `P` and choose `CodeSee: Open Review Map`. This will open a visual representation of the pull request.

- Use your mouse to drag the map around.
- Use `Ctrl` + your mouse wheel to zoom in and out.
- Click on a file to view its dependencies and tune out the rest.
- Double-click on a file to open a diff view.
- Right-click on a file to mark it as viewed—this will be reflected in GitHub.

#### GitHub Pull Request Sidebar

When viewing a file inside the sidebar of the GitHub Pull Request & Issues extensions, you can create a Review Map of those changes without checking out the branch:

1. Open the [GitHub Pull Requests and Issues](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) sidebar.
2. Choose a pull request under any category. The "All Open" category is a good place to start.
3. Expand the pull request you want to view and open a file within.
4. Open a Review Map using the command palette and choose `CodeSee: Open Review Map`. This will open a visual representation of the pull request.

![Review Map within the GitHub extension](https://s3.us-east-2.amazonaws.com/maps.codesee.io/github_extension.gif)

### Feedback 
Feel free to provide feedback or submit feature requests to [support@codesee.io](mailto:support@codesee.io).
