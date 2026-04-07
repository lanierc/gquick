
# gquick

**gquick** is a minimalist CLI tool designed to automate the repetitive "add-commit-push" workflow in Git. It allows you to stage changes, create a commit, and push to your remote repository with a single command.

---

### Features

* **One-Command Workflow**: Replaces `git add .`, `git commit -m "..."`, and `git push` with a single shortcut.
* **Process Tracking**: Provides clear, color-coded feedback for each stage of the Git process.
* **Error Handling**: Stops execution if a step fails (e.g., if there are no changes to commit or if the push fails).
* **Lightweight**: A simple Bash script with zero overhead.

---

### Installation

#### Arch Linux (AUR)
The easiest way to install on Arch Linux is via the AUR:
```bash
yay -S gquick-git
```

#### Manual Installation
For other Linux distributions, clone the repository and create a symbolic link:
```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/gquick.git
cd gquick
chmod +x gquick
sudo ln -s $(pwd)/gquick /usr/bin/gquick
```

---

### Usage

Simply provide your commit message as an argument:

```bash
gquick "your commit message here"
```

#### What happens under the hood:
1. `git add .` is executed to stage all changes.
2. `git commit -m "your message"` is executed.
3. `git push` is executed to update the remote repository.

---

### Requirements

* `git`
* `bash`

---

### License

This project is licensed under the MIT License.

---

> **Note:** Make sure you are inside a Git repository before running `gquick`.
