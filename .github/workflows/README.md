# GitHub Actions Setup

## Publish Release Workflow

This workflow automates the release publishing process by:
1. Fetching the changelog from a private repository's release page
2. Updating the CHANGELOG.md in this repository
3. Creating a new GitHub release (ready for manual app file upload)

### Prerequisites

Since you own both repositories, the workflow uses the automatic `GITHUB_TOKEN` - no personal access token needed!

#### Add Repository Variable

1. Go to your repository Settings > Secrets and variables > Actions > Variables tab
2. Click "New repository variable"
3. Name: `PRIVATE_REPO_NAME`
4. Value: Your private repo in format `owner/repo-name` (e.g., `myusername/my-private-repo`)
5. Click "Add variable"

That's it! The workflow will automatically use your GitHub account's access to read from the private repo.

### Usage

#### Manual Trigger

1. Go to Actions tab in your repository
2. Select "Publish Release" workflow
3. Click "Run workflow"
4. (Optional) Enter a version tag (e.g., `v1.3.3`)
   - If left empty, it will use the latest release tag from the private repo
5. Click "Run workflow"

The workflow will:
- Fetch the changelog from the private repo's release page
- Update CHANGELOG.md with the new entry at the top
- Commit and push the changes
- Create a new GitHub release
- Print a URL where you can manually upload your app file

### Troubleshooting

**Error: "Could not fetch latest release from private repo"**
- Verify the `PRIVATE_REPO_NAME` variable is correct (format: `owner/repo-name`)
- Check that the private repo has at least one release
- Ensure you have access to the private repository with your GitHub account

**Error: "Could not fetch release notes for version X"**
- Verify the version tag exists in the private repository
- Check that the release has content in its body

**Error: "Resource not accessible by integration"**
- This means the automatic `GITHUB_TOKEN` doesn't have access to the private repo
- Make sure you own both repositories under the same GitHub account
- If the repos are under different accounts, you'll need to use a Personal Access Token instead

**No changes to commit**
- The changelog entry already exists in CHANGELOG.md
- This is normal if you're re-running the workflow with the same version
