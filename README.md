# ALX Advanced Git Project – Git-Flow

## 📌 Overview
Git-Flow is a branching model for Git, proposed by Vincent Driessen, that helps developers manage features, releases, and hotfixes in a consistent and scalable way. It introduces well-defined roles for branches and helps teams coordinate code changes more effectively. Git-Flow is particularly beneficial for large-scale projects where multiple developers work simultaneously on various aspects of the codebase.

### 🔑 Primary Branch Types
- **main (or master)** – production-ready code  
- **develop** – ongoing development  
- **feature/*** – new features in progress  
- **release/*** – preparation for production releases  
- **hotfix/*** – critical bug fixes on the main branch  

---

## 🎯 Relevance in the Development Process
Git-Flow improves:
- **Code organization** by clearly separating development stages  
- **Team collaboration** through structured branching and merging workflows  
- **Code stability** by allowing features to be tested and integrated before reaching production  
- **Release management** by isolating release-specific tasks  

Git-Flow is widely adopted in agile and CI/CD environments, ensuring seamless integration and deployment pipelines while reducing conflicts and regression bugs.

---

## 🎓 Learning Objectives
By the end of this project, learners should be able to:
- Understand the purpose and structure of Git-Flow.  
- Identify the different branch types and their roles.  
- Apply Git-Flow in real-world collaborative development projects.  
- Manage feature development, hotfixes, and release cycles using Git best practices.  

---

## 🏆 Learning Outcomes
Learners will be able to:
- Explain how Git-Flow helps manage large codebases and team contributions.  
- Create and manage branches following the Git-Flow model.  
- Use Git commands to initiate features, releases, and hotfix branches.  
- Integrate Git-Flow into CI/CD pipelines for automated testing and deployments.  

---

## ✅ Git-Flow Best Practices

| Best Practice | Description |
|---------------|-------------|
| Start with develop | Always branch off from `develop` for new features, not `main`. |
| Feature Isolation | Keep each feature in its own branch to reduce merge conflicts. |
| Merge via Pull Requests | Use pull/merge requests for all merges to ensure code review. |
| Keep main clean | Only production-ready code goes into `main`. Never push untested code here. |
| Tag Releases | Use Git tags on the `main` branch to mark official release points. |
| Use hotfix/* for urgent bugs | Apply emergency fixes directly to `main` via a hotfix branch and merge them back into `develop`. |
| Document your workflow | Maintain clear documentation of your Git-Flow in your project’s README or internal wiki. |

---

## 💻 Common Git-Flow Commands

```bash
git flow init                   # Initialize Git-Flow
git flow feature start <name>   # Start a new feature branch
git flow feature finish <name>  # Finish feature and merge into develop
git flow release start <x.x.x>  # Start a release branch
git flow release finish <x.x.x> # Merge release into main and develop
git flow hotfix start <x.x.x>   # Start a hotfix branch
git flow hotfix finish <x.x.x>  # Finish hotfix and merge into main & develop
````

---

## 📂 Project Tasks

### **Task 0: Setting up GitFlow**

* Install `git-flow` if not already installed.
* Create an empty repository `ALXprodev-advanced_git`.
* Clone the repository locally.
* Create and push the `develop` branch.
* Initialize Git-Flow (`git flow init -d`).
* Create an empty `README.md` file, commit, and push.

---

### **Task 1: Creating a Feature Branch**

* Create a new feature branch `feature/implement-login` from `develop`.
* Inside it, create a `login-page/README.md` file with the message:

  ```
  Login Feature Coming soon
  ```
* Commit with message:

  ```
  feat: scaffolding login page
  ```
* Push to GitHub.

---

### **Task 2: Creating a Release Branch**

* Create a new feature branch `feature/implement-signup` from `develop`.
* Add `signup-page/README.md` with the message:

  ```
  feature coming soon
  ```
* Commit and push changes.
* Merge both features into `develop` (resolve conflicts if any).
* Create a release branch `release/1.0.0`.
* Modify `signup-page/README.md` to include:

  ```
  data requirements: email, firstName, lastName, profilePic
  ```
* Commit and push changes.
* Merge the release branch into both `main` and `develop`.
* Tag the release `v1.0.0` and push tags to remote.

---

### **Task 3: Git Hooks and Automation**

* Implement a **pre-commit hook** in `.git/hooks/pre-commit` to ensure each directory has a `README.md`.
* Implement a **post-merge hook** in `.git/hooks/post-merge` to log merges into the `main` branch.

---

### **Task 4: Manual Review**

* Manual review will be conducted to assess your repository.
* Ensure all files and branches follow Git-Flow standards.

---

## 📝 Project Assessment

* **Manual reviews** will form the core evaluation.
* To get full credit:

  * ✅ Complete your project on time.
  * 📄 Submit all required files.
  * 🔗 Generate your review link.
  * 👥 Have peers review your work.

⚠️ **Note:** If the deadline passes, you won’t be able to generate your review link.

---

## 🎉 Final Note

We’re here to support your learning journey. Happy coding with Git-Flow! 🚀
