## PR Checklist

Before requesting a review, please confirm the following:

### 📝 Description
### ✅ The Honor System Checklist
- [ ] I created a feature branch for this work and did not commit directly to `main`.
- [ ] I have done a self-review of my own code before opening this PR.
- [ ] I have moved the corresponding card on the GitHub Project Board to "Testing".

### 🔒 Security & Secrets
- [ ] I verified that no `.env` files or API keys were accidentally tracked in this commit.
- [ ] Database connection strings (e.g., PostgreSQL credentials) are not hardcoded anywhere in the code.
- [ ] No deployment keys or infrastructure state files (like `.tfstate`) are included in this PR.

### 🛠️ Backend & Code Quality
- [ ] I have tested this code locally and it works as expected.
- [ ] If I added new dependencies to `package.json`, they are necessary and documented.
- [ ] Any new database schemas, migrations, or queries have been thoroughly verified.
- [ ] I removed any unnecessary `console.log()` debugging statements.

### 🏗️ Infrastructure & Deployment (If applicable)
- [ ] I ran `terraform fmt` to format any infrastructure configuration changes.
- [ ] Infrastructure code has been validated and runs without errors.

### 🤝 Review Request
- [ ] I have tagged at least one teammate to review this Pull Request.
