# Contributing to the Policy Review Process

Thank you for participating in the Lehigh community policy review process. This guide explains how to engage with draft policies and how the approval workflow operates.

---

## For Community Members: Reviewing a Draft Policy

### Step 1 — Find the draft

All draft policies under active review are listed as open **Pull Requests**:

👉 [View open policy review PRs](../../pulls?q=is%3Aopen+label%3Apolicy-review)

Each PR includes:
- A summary of what is being changed and why
- The full text of the proposed policy (or a diff showing changes from the current version)
- A **review deadline**

### Step 2 — Leave feedback

1. Open the Pull Request for the policy you want to review.
2. Click the **"Files changed"** tab to see exactly what is being proposed.
3. To leave a comment on a specific line, hover over it and click the **blue `+` icon**.
4. To leave a general comment, scroll to the bottom of the PR and use the comment box.

> **Note:** You need a free [GitHub account](https://github.com/signup) to leave comments. You do not need an account to read drafts.

### Step 3 — Wait for a response

The policy administrator will review all comments and may revise the draft. You will be notified of responses if you are subscribed to the PR (click **"Subscribe"** on the right sidebar).

---

## For Policy Administrators: Managing the Workflow

### Creating a new draft

1. Create a new branch from `main`:
   ```bash
   git checkout main
   git pull
   git checkout -b draft/<policy-name>
   ```

2. Add or modify the policy file in `drafts/`:
   ```bash
   cp drafts/draft-template.md drafts/DRAFT-<policy-name>.md
   # Edit the file
   git add drafts/DRAFT-<policy-name>.md
   git commit -m "Add draft: <policy-name>"
   git push origin draft/<policy-name>
   ```

3. Open a Pull Request from `draft/<policy-name>` → `main` on GitHub.
   - Use the PR template to fill in the review deadline and summary.
   - Add the `policy-review` label.

### Approving and adopting a policy

Once the review period is complete and the policy is approved:

1. Move/copy the draft file to the `policies/` directory:
   ```bash
   cp drafts/DRAFT-<policy-name>.md policies/<policy-name>.md
   # Remove the draft file
   git rm drafts/DRAFT-<policy-name>.md
   git add policies/<policy-name>.md
   git commit -m "Adopt policy: <policy-name>"
   ```

2. Merge the Pull Request into `main` on GitHub.

3. The old version is automatically preserved in Git history — no extra steps needed.

### Viewing old versions

```bash
# See the history of a policy file
git log --oneline -- policies/<policy-name>.md

# View the policy at a specific past commit
git show <commit-hash>:policies/<policy-name>.md

# Compare two versions
git diff <old-commit>..<new-commit> -- policies/<policy-name>.md
```
