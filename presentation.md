---
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

![bg left:40% 80%](https://marp.app/assets/marp.svg)

# **Magic of GitHub Actions: Automating Tasks**

Open-source Maintainer, GitHub

Tehran Lug - 26 Feb 2027

https://github.com/basemax

---

# **What is GitHub Actions?**
- A CI/CD service by GitHub
- Automates workflows directly in GitHub repositories
- Runs on GitHub-hosted or self-hosted runners

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
- **Automated Testing**: Run unit tests before merging PRs
- **Static Analysis**: Linting and security scans
- **Deployment**: Push Docker images, deploy web apps

---

# **Conclusion**
- GitHub Actions simplifies automation
- CI/CD improves software quality and deployment speed
- Self-hosted runners enable custom workflows

---

# **Q&A**
Let's discuss! 🚀

