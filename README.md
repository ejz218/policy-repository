# Lehigh Policy Repository

This repository contains the **authoritative copies** of institutional policies. All policies are public and version-controlled using Git, so the full history of every policy is always accessible.

---

## 📄 Current Policies

All approved, in-effect policies live in the [`policies/`](./policies/) directory on the `main` branch.

| Policy | Description |
|--------|-------------|
| *(Add policies here as they are adopted)* | |

---

## 📝 Drafts Under Community Review

Proposed modifications to policies are posted as **Pull Requests** on this repository. Anyone can read and comment on open PRs — no GitHub account is required to view them; a free account is needed to leave a comment.

👉 **[View all open draft PRs](../../pulls?q=is%3Aopen+label%3Apolicy-review)**

Drafts in progress are also available in the [`drafts/`](./drafts/) directory.

---

## 🔄 How the Process Works

1. **A draft is created** — A proposed policy change is written and posted as a Pull Request for community review.
2. **Community reviews** — Members of the Lehigh community read the draft and leave comments on the PR.
3. **Revisions are made** — The policy author may revise the draft based on feedback.
4. **Approval & adoption** — Once approved, the PR is merged into `main`, replacing the old policy text.
5. **History is preserved** — The previous version of the policy is always accessible via Git history (see below).

---

## 🕰️ Viewing Old Policy Versions

Because this repository uses Git, every previous version of every policy is permanently preserved.

**On GitHub:**
- Navigate to a policy file (e.g., `policies/acceptable-use.md`)
- Click **"History"** (top right of the file view) to see all past versions
- Click any commit to see the exact text at that point in time

**Via command line:**
```bash
# View the full history of a specific policy
git log --oneline -- policies/acceptable-use.md

# View the policy as it was at a specific commit
git show <commit-hash>:policies/acceptable-use.md
```

---

## 📬 Questions & Contact

For questions about a specific policy or the review process, please open a [GitHub Issue](../../issues) or contact the policy administrator directly.
