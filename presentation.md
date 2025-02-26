---
theme: gaia
paginate: true
backgroundColor: #000
color: #fff
colorPreset: dark
footer: Tehran Lug 2/27/2025
---

![bg left:30% 70%](logo.png)

# **Magic of GitHub Actions: Automating Tasks**

<!-- Seyyed Ali Mohammadiyeh -->
<!-- (MAX BASE) -->

Tehran Lug - 27 Feb 2027

---

# **About me**

**Seyyed Ali Mohammadiyeh (Max Base)**

Open-source Maintainer, GitHub
Software Engineer
CTO, asrez
<!-- Department of Pure Mathematics, Faculty of Mathematical Sciences, University of Kashan -->

maxbasecode@gmail.com
<!-- alim@kashanu.ac.ir -->

---

# **About me**

**Seyyed Ali Mohammadiyeh (Max Base)**

- **GitHub**: [https://github.com/basemax](https://github.com/basemax)
- **Experience**: Over 10 years in software development and programming
- **Background**: Pure-mathematics and applied mathematics, with research experience

---

# **What is GitHub Actions?**
- A CI/CD service by GitHub
- Automates workflows directly in GitHub repositories

---

# **Why Use GitHub Actions?**
- Automates testing, deployment, and workflows
- Reduces manual work
- Provides seamless integration with GitHub repositories

---

# **What is CI/CD?**
- CI (Continuous Integration): Merging code frequently & running tests automatically
- CD (Continuous Deployment/Delivery): Automatically deploying tested code to production

---

# **Benefits of CI/CD**
- Faster development cycles
- Improved code quality
- Automatic rollback in case of failure

---

# **What is a Pipeline?**
- A sequence of automated steps
- Includes build, test, and deployment stages
- Can be customized as per project needs

---

# **How Does a CI/CD Pipeline Work?**
1. Developer pushes code
2. Automated tests run
3. Code is built and packaged
4. Deployment is triggered (if applicable)

---

# **Components of GitHub Actions**
- **Workflows**: Define automation process
- **Events**: Triggers for workflows (push, pull request, etc.)
- **Jobs**: Tasks running in parallel or sequentially
- **Steps**: Individual commands within a job
- **Actions**: Pre-built or custom scripts

---

# **Workflow Example**
```yaml
name: CI
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Run a script
        run: echo "Hello, GitHub Actions!"
```

---

# **Events That Trigger Workflows**
- `push` or `pull_request`
- Issues and comments
- Scheduled CRON jobs
- Manual trigger (`workflow_dispatch`)

---

# **Understanding Jobs**
- A workflow can have multiple jobs
- Jobs can run in parallel or sequentially
- Example:
```yaml
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - run: npm test
  deploy:
    needs: test
    runs-on: ubuntu-latest
    steps:
      - run: npm run deploy
```

---

# **What are GitHub Runners?**
- Machines that execute workflows
- Two types:
  - **GitHub-hosted** (Linux, macOS, Windows)
  - **Self-hosted** (Custom machine or cloud server)

---

# **How to Create a Self-hosted Runner**
1. Go to GitHub repository settings
2. Navigate to `Actions` > `Runners`
3. Download and configure the runner
4. Start the runner and register it with GitHub

---

# **Example Use Cases**
- Running automated tests
- Deploying applications
- Sending notifications (Slack, Email)
- Automating documentation generation
- Running security scans

---

# **Deploying with GitHub Actions**
- Example deployment job:
```yaml
name: Deploy
on: push
to:
  branches: [main]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - run: ./deploy.sh
```

---

# **Using Secrets in GitHub Actions**
- Store API keys, passwords securely
- Access them using `${{ secrets.SECRET_NAME }}`
- Example:
```yaml
jobs:
  deploy:
    steps:
      - run: echo "Deploying with ${{ secrets.API_KEY }}"
```

---

# **Matrix Strategy for Multiple Environments**
```yaml
jobs:
  test:
    strategy:
      matrix:
        os: [ubuntu-latest, windows-latest, macos-latest]
    runs-on: ${{ matrix.os }}
    steps:
      - run: echo "Running on ${{ matrix.os }}"
```

---

# **Advanced Workflow Features**
- Caching dependencies
- Running workflows conditionally
- Handling workflow concurrency

---

# **Security Best Practices**
- Use GitHub’s OIDC authentication for cloud providers
- Rotate secrets regularly
- Restrict permissions of GitHub tokens

---

# **Monitoring Workflow Execution**
- View logs in GitHub Actions UI
- Use `job.status` for conditional steps
```yaml
jobs:
  test:
    steps:
      - run: echo "Running tests"
      - if: failure()
        run: echo "Tests failed!"
```

---

# **Real-World Examples**

1) https://github.com/BaseMax/React-Auto-Build-GitHub-Actions
2) https://github.com/BaseMax/github-actions-nextjs-build-deploy
3) https://github.com/BaseMax/AndroidAutoBuildAPK
4) https://github.com/BaseMax/GitHubAction-Jekyll-SFTP-Deploy-Password
5) https://github.com/BaseMax/GitHubAction-SFTP-Deploy-Password
6) https://github.com/BaseMax/AutoInviteToOrgByIssueComment

---

# **Real-World Examples**

7) https://github.com/BaseMax/AutoInviteToOrgByStar
8) https://github.com/BaseMax/github-actions-cpanel-php-ftp
9) https://github.com/BaseMax/github-actions-compile-golang
10) https://github.com/BaseMax/github-actions-compile-c
11) https://github.com/BaseMax/github-actions-update-push
12) https://github.com/BaseMax/github-actions-create-tag

---

# **Real-World Examples**

13) https://github.com/BaseMax/github-actions-upload-temp-file
14) https://github.com/BaseMax/github-actions-create-release
15) https://github.com/BaseMax/github-actions-monitor-issues
16) https://github.com/BaseMax/github-actions-run-docker-compose
17) https://github.com/BaseMax/github-actions-run-dockerfile
18) https://github.com/BaseMax/github-actions-compile-rust

---

# **Real-World Examples**

19) https://github.com/BaseMax/github-actions-react-deploy-tailwindcss-sftp
20) https://github.com/BaseMax/github-actions-react-deploy-linux-sftp
21) https://github.com/BaseMax/github-actions-react-build-linux-sftp
22) https://github.com/BaseMax/github-actions-file-linux-ssh-sftp

---

# **Cool builds**

| ![](coffee.jpg) | ![](wireless-coffee.jpg) |
|-----------------|--------------------------|

[Using GitHub Actions to Brew Coffee](https://hackaday.com/2022/12/10/using-github-actions-to-brew-coffee/)
[Hacking Bluetooth to Brew Coffee on GitHub Actions Part 1](https://grack.com/blog/2022/12/01/hacking-bluetooth-to-brew-coffee-on-github-actions-part-1/)

---

# **Q&A**
Let's discuss! 🚀

maxbasecode@gmail.com

github.com/basemax

t.me/MAX_BASE
