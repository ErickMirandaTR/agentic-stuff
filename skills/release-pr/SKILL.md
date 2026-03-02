---
name: release-pr
description: Create release and develop PRs when the user provides a user story (number), branch name, and release branch, and has the documents to be committed already staged; perform the following steps using Git and Github.
compatibility: Requires git and either GitHub CLI (gh) or a GitHub MCP server. Optionally uses Azure DevOps MCP for work item URL resolution.
metadata:
  author: ErickMirandaTR
  version: "1.1"
---

### Step 1: Create the feature/bug fix branch from develop
1. Fetch the latest from origin.
2. Create a new branch from develop using one of the formats:
feature/<userStory>-<descriptiveName>
bug/<userStory>-<descriptiveName>
or the exact branchName provided.
3. Stage any currently staged files into a commit with a meaningful message referencing the work item, following the format:
[AB:<userStory>] <Short imperative summary>
Example:
[AB#12345] Add validation for empty invoice lines
4. Push the branch to origin.

### Step 2: Create PR #1 (feature/bug branch → develop)
1. Create a Pull Request from the new branch into develop using the following PR title format:
[AB#<userStory>] <Short, imperative summary of the change>
Examples:
[AB#73621] Feature: Implement user permission check in invoice flow
[AB#81230] Bug: Fix null reference crash when loading settings
[AB#55110] Refactor: Pricing logic for consistency
3. Resolve Azure DevOps work item URL
If Azure DevOps MCP is active: call MCP to get the canonical item URL.
Else: fallback to <https://dev.azure.com/tr-tax/TaxProf/<adoProject>/_workitems/edit/<userStory>>.
2. Link the work item (e.g., `AB#<userStory>`, use <resolved-ado-url> to make a Markdown link) in the PR description within work item section. Follow additional fields required by the repo template (if detected)

### Step 3: Create the cherry-pick branch from the release branch
1. Create a new branch from the specified release branch (e.g., `release/releaseyyyy.mm.x`) with a similar name: `<feature|bug>/<userStory>-<descriptiveName>` (appending a suffix like `-release` to differentiate).
2. Cherry-pick the commit SHA from Step 1 onto this new branch.
3. Resolve any conflicts if possible, or flag them to the user.
4. Push the branch to origin.

### Step 4: Create PR #2 (cherry-pick branch → release branch)
1. Create a Pull Request from the cherry-pick branch into the release branch.
2. Link the same work item `AB#<userStory>` in the PR description.
3. Add a cross-reference to PR #1 in the description of PR #2 within work item section, and update PR #1's description to reference PR #2 within work item section (e.g., `- develop PR #<id>` or `- release PR #<id>`)

### Output
Provide the user with:
- Both branch names created
- Both PR URLs/numbers
- The commit SHA that was cherry-picked
- Confirmation of work item linking and cross-references