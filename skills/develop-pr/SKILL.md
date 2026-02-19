---
name: develop-pr
description: Create a develop PR when the user provides a user story (number) and branch name, and has the documents to be committed already staged; perform the following steps using Git and Github.
compatibility: Requires git and either GitHub CLI (gh) or a GitHub MCP server.
metadata:
  author: ErickMirandaTR
  version: "1.0"
---

### Step 1: Create the feature/bug fix branch from develop
1. Fetch the latest from origin.
2. Create a new branch based on `develop` with the naming convention: `<feature|bug>/<userStory>-<descriptiveName>` or `branchName`
3. Stage any currently staged files into a commit with a meaningful message referencing the work item.
4. Push the branch to origin.

### Step 2: Create PR #1 (feature/bug branch → develop)
1. Create a Pull Request from the new feature/bug branch into `develop`.
2. Link the work item (e.g., `AB#<userStory>`) in the PR description within work item section.


### Output
Provide the user with:
- Branch name created
- PR URL/number
- Confirmation of work item linking