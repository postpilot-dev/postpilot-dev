# GitHub Actions Setup

## Publish Release Workflow

This workflow automates the release publishing process by:
1. Fetching the changelog from a private repository's release page
2. Updating the CHANGELOG.md in this repository
3. Creating a new GitHub release (ready for manual app file upload)

### Prerequisites

#### 1. Create a Personal Access Token (PAT)

The workflow needs access to your private repository, which requires a PAT:

1. Go to GitHub Settings > Developer settings > Personal access tokens > Tokens (classic)
2. Click "Generate new token (classic)"
3. Give it a name like "postpilot-release-workflow"
4. Select scopes: **`repo`** (full control of private repositories)
5. Click "Generate token" and copy the token value

#### 2. Add Repository Secret

1. Go to your repository Settings > Secrets and variables > Actions > Secrets tab
2. Click "New repository secret"
3. Name: `PRIVATE_REPO_TOKEN`
4. Value: Paste your PAT from step 1
5. Click "Add secret"

#### 3. Add Repository Variable

1. Go to your repository Settings > Secrets and variables > Actions > Variables tab
2. Click "New repository variable"
3. Name: `PRIVATE_REPO_NAME`
4. Value: Your private repo in format `owner/repo-name` (e.g., `myusername/my-private-repo`)
5. Click "Add variable"

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

**Error: "gh: Not Found (HTTP 404)"**
- Verify the `PRIVATE_REPO_TOKEN` secret is set correctly with a valid PAT
- Ensure the PAT has `repo` scope enabled
- Check that the `PRIVATE_REPO_NAME` variable is correct (format: `owner/repo-name`)
- Verify you have access to the private repository

**Error: "Could not fetch latest release from private repo"**
- Verify the `PRIVATE_REPO_NAME` variable is correct (format: `owner/repo-name`)
- Check that the private repo has at least one release
- Ensure your PAT has access to the private repository

**Error: "Could not fetch release notes for version X"**
- Verify the version tag exists in the private repository
- Check that the release has content in its body

**Error: "Resource not accessible by integration"**
- This means the `PRIVATE_REPO_TOKEN` doesn't have sufficient permissions
- Regenerate your PAT with the `repo` scope enabled

**No changes to commit**
- The changelog entry already exists in CHANGELOG.md
- This is normal if you're re-running the workflow with the same version
