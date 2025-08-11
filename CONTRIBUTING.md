# Contributing to Term

Thank you for your interest in contributing to Term! This guide will help you get started with the contribution process.

---

## 🚀 Quick Start

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:

   ```bash
   git clone https://github.com/YOUR_USERNAME/term.git
   cd term
   ```
3. **Set up the development environment**:

   ```bash
   # Install Node.js dependencies
   npm install

   # Install Rust (if not already installed)
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   source ~/.cargo/env

   # Install Tauri CLI
   cargo install tauri-cli
   ```
4. **Create a new branch** for your feature:

   ```bash
   git checkout -b feat/your-feature-name
   ```

---

## 📋 Development Guidelines

### Code Style

* **Frontend**: TypeScript best practices, functional components + hooks
* **Backend**: Rust conventions, run `cargo fmt` before commits
* **Commits**: Follow [Conventional Commits](https://www.conventionalcommits.org/)
* **DCO**: All commits must be signed off (details below)

### Testing

* Run: `npm test`
* Add tests for new features
* Ensure cross-platform compatibility

### Documentation

* Update README.md for major changes
* Add JSDoc for new functions
* Maintain inline comments

---

## ⚖️ Developer Certificate of Origin (DCO)

### What is DCO?

The DCO is a lightweight way for contributors to certify they have the right to submit code under the project's license.

### Required Sign-off

**All commits must be signed off.** This is enforced by CI/CD.

#### New Commits

```bash
git commit -s -m "feat: add new feature"
```

#### Existing Commits

```bash
# Last commit
git commit --amend -s

# Multiple commits
git rebase --signoff HEAD~3

# Entire branch
git rebase --signoff main
```

#### Manual Sign-off

```
Signed-off-by: Your Name <your.email@example.com>
```

#### Git Config

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --global alias.cs 'commit -s'
```

---

## 🔄 Contribution Workflow

### 1. Create an Issue (Optional)

* Check existing issues
* Bugs: include steps, environment, logs
* Features: describe use case + solution

### 2. Development

```bash
git remote add upstream https://github.com/zoxilsi/term.git
git fetch upstream
git checkout main
git merge upstream/main

# Feature branch
git checkout -b feat/amazing-feature

# Signed commit
git add .
git commit -s -m "feat: amazing feature"

npm test
npm run lint
npm run build

git push origin feat/amazing-feature
```

### 3. Pull Request

1. Open PR on GitHub
2. Fill PR template
3. Ensure CI passes
4. Address review feedback

---

## 🧪 Testing Your Changes

### Frontend

```bash
npm test
npm run test:watch
npm run test:coverage
```

### Backend

```bash
cd src-tauri
cargo test
cargo test -- --nocapture
```

### Manual

```bash
npm run tauri dev
```

---

## 🏷️ Commit Message Format

```
<type>[scope]: description

[optional body]

[optional footer]
Signed-off-by: Your Name <your.email@example.com>
```

Types:

* `feat` | `fix` | `docs` | `style` | `refactor` | `test` | `chore` | `ci` | `perf` | `build`

Examples:

```bash
git commit -s -m "feat: add AI autocompletion"
git commit -s -m "fix: resolve output formatting"
```

---

## 🐛 Reporting Issues

### Bugs

Include:

* Steps to reproduce
* Expected vs actual
* Environment details
* Screenshots/logs

### Features

Include:

* Use case
* Proposed solution
* Alternatives
* Extra context

---

## 📞 Getting Help

* **Issues**: Bug reports & feature requests
* **Discussions**: Q\&A & ideas
* **Reviews**: Feedback on PRs

---

## 🎯 Areas for Contribution

* Bug fixes
* Features
* Documentation
* Testing
* UI/UX
* Performance improvements

---

## ⚠️ Notes

1. PRs without DCO will be rejected
2. All code changes need review
3. Breaking changes require discussion
4. Maintain backwards compatibility
5. Test on multiple OS where possible

---

## 🙏 Thank You

Your contributions make Term better for everyone!

For more DCO details, see [.github/DCO.md](.github/DCO.md).
