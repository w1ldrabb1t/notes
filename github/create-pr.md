# Guide on How to Make a Pull Request on GitHub

This guide explains how to suggest an edit to a repository's `README.md` file on GitHub. It assumes you have already cloned the repository to your local machine.

---

## **1. Create a New Branch**
To make your changes in isolation, create a new branch:

1. Open your terminal or command prompt and navigate to the local directory of the cloned repository.
2. Create and switch to a new branch:
   ```bash
   git checkout -b suggest-readme-edit
   ```
   Replace `suggest-readme-edit` with a branch name that reflects your changes.

---

## **2. Make Your Changes**
1. Open the `README.md` file in your favorite text editor or IDE.
2. Make the necessary edits to the specific line(s).
3. Save your changes.

---

## **3. Stage and Commit Your Changes**
1. Stage the `README.md` file:
   ```bash
   git add README.md
   ```
2. Commit your changes with a clear message:
   ```bash
   git commit -m "Suggested edits to README.md"
   ```

---

## **4. Push Your Branch to the Remote Repository**
1. Push your branch to the remote GitHub repository:
   ```bash
   git push origin suggest-readme-edit
   ```
   Replace `suggest-readme-edit` with the branch name you created earlier.

---

## **5. Create a Pull Request (PR) on GitHub**
1. Go to the repository's page on GitHub in your browser.
2. GitHub should detect your recently pushed branch and display a "Compare & pull request" button. Click it.  
   If you don’t see this button:
   - Go to the **Pull Requests** tab.
   - Click the **New pull request** button.
   - Select your branch (`suggest-readme-edit`) from the dropdown menu as the **source** branch.
3. Add a title and description for your pull request explaining your changes.
4. Click **Create pull request**.

---

## **6. Wait for Review**
The repository maintainers will review your pull request. They might:
- Approve and merge it.
- Request changes or further edits.

---

## **7. Address Feedback (If Needed)**
If the maintainers request changes:

1. Make the requested changes in your local branch.
2. Stage, commit, and push the changes:
   ```bash
   git add README.md
   git commit -m "Addressed feedback"
   git push origin suggest-readme-edit
   ```
3. The changes will automatically update your existing pull request.

---

## **8. Clean Up (Optional)**
Once your pull request is merged or closed:

1. Switch back to the main branch locally:
   ```bash
   git checkout main
   ```
   (Replace `main` with `master` or another branch name if applicable.)
2. Delete your branch:
   ```bash
   git branch -d suggest-readme-edit
   ```
3. Optionally, delete the remote branch:
   ```bash
   git push origin --delete suggest-readme-edit
   ```

---



### **If You Do NOT Have Write Access (Fork and Pull Request)**

If you are **not a collaborator**, you cannot push directly. Instead, you must:

1. **Fork the Repository** 
    - Go to the public repo on GitHub.
    - Click **Fork** (top-right) to create your own copy.

2. **Clone Your Fork Using SSH**
    - Copy the SSH URL from your fork (not the original repo).
    - Clone it:
        `git clone git@github.com:your-username/repository.git`
 
        _(Replace `your-username` with your GitHub username.)_
3. **Create a Branch and Make Changes**
    `git checkout -b my-feature-branch`

    - Edit files.
    - Commit changes:

	`git add . git commit -m "Added a new feature"`
 
4. **Push the Changes to Your Fork**

	`git push origin my-feature-branch`

	`git remote set-url origin git@github.com:username/repository.git`


5. **Create a Pull Request (PR)**
    - Go to your fork on GitHub.
    - GitHub will suggest creating a **Pull Request (PR)** to the original repository.
    - Click **Compare & pull request**.
    - Add a description and submit it.

6. **Wait for Review**

    - The repository owner will review your PR.
    - If approved, they will merge it.
    - If changes are needed, update your branch and push again:
