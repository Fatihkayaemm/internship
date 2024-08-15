# internship
This is Repo
# Task-1
https://vimeo.com/manage/videos/997910031

# Task-2/3
Step 1: Clone the Repository

	1. Open Terminal or Command Prompt:
		• Use Terminal (on macOS/Linux) or Command Prompt (on Windows) to run commands.
	2. Find the Repository URL:
		• Go to your project’s page on GitHub (or another platform) and click the “Code” button.
		• Copy the repository’s HTTPS URL, which looks something like this: https://github.com/username/repository-name.git.
	3. Clone the Repository:
		• Run the following command in the terminal to clone the repository to your local machine:
		>> git clone https://github.com/username/repository-name.git
		• This command will copy the repository to your computer.

Step 2: Create a README File

	1. Navigate to the Project Directory:
	 	• Move into the directory of the cloned repository:
		>> cd repository-name
	2. Create the README File:
		• Use the touch command to create a new README.md file:
		>> touch README.md
	3. Edit the README File:
		• Open the README.md file with a text editor and add the following content:
		>> # Project Name

		This project demonstrates how to clone a Git repository and create a README file.

		## Steps

		1. **Cloning the Repository**:
    		- The repository URL was copied from the GitHub page.
    		- The repository was cloned to the local machine using the following command:
    		```bash
    		git clone https://github.com/username/repository-name.git
    		```

		2. **Creating a README File**:
    		- Changed directory to the cloned repository:
    		```bash
    		cd repository-name
    		```
    		- Created the `README.md` file with the following command:
    		```bash
    		touch README.md
    		```
    		- Added information about the project to the README file.

		## Notes

		This README file was created to practice basic Git commands and file creation.

	4. Save and Close the File:
		• Save the file and close your text editor.


Step 3: Add and Commit the README File to Your Repository

	1. Stage the Changes:
		• Add the README.md file to the staging area:
		>> git add README.md
	2. Commit the Changes:
	 	• Commit the staged changes with a descriptive message:
		>> git commit -m "Added README file documenting the cloning process"
	3. Push the Changes to the Remote Repository:
		• Push the commit to the remote repository on GitHub (or another platform):
		>> git push origin master

=============================================================
# Task 4

**Creating Separate SSH Connections for Both Your Personal and Company GitHub Accounts**

**1. Generate SSH Keys**

You need to create separate SSH keys for your personal and company GitHub accounts. You can do this using the terminal or command line.

a) **Generate SSH Key for Your Personal Account:**

```bash
ssh-keygen -t ed25519 -C "your-email@example.com" -f ~/.ssh/id_ed25519_personal
```

This command will generate an SSH key pair named `id_ed25519_personal` in the `~/.ssh/` directory.

b) **Generate SSH Key for Your Company Account:**

```bash
ssh-keygen -t ed25519 -C "company-email@example.com" -f ~/.ssh/id_ed25519_company
```

This command will generate an SSH key pair named `id_ed25519_company` in the `~/.ssh/` directory.

**2. Add SSH Keys to GitHub**

a) **Add Your Personal SSH Key:**

1. Copy the content of your personal SSH key using the following command in the terminal:

```bash
cat ~/.ssh/id_ed25519_personal.pub
```

2. Log in to GitHub, click on your profile picture in the top right corner, and go to "Settings."

3. Navigate to the “SSH and GPG keys” section and click the “New SSH key” button.

4. In the “Title” field, enter a name for your key (e.g., “Personal SSH Key”), paste the key content, and click the “Add SSH key” button.

b) **Add Your Company SSH Key:**

1. Copy the content of your company SSH key using the following command in the terminal:

```bash
cat ~/.ssh/id_ed25519_company.pub
```

2. Log in to your company's GitHub account and follow the same steps to add this SSH key.

**3. Edit the SSH Config File**

To manage both SSH keys, you need to edit the `~/.ssh/config` file. If the file doesn’t exist, you can create it. Add the following lines to the file:

```bash
# For Personal Account
Host github.com-personal
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_personal

# For Company Account
Host github.com-company
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_company
```

With this configuration, you can use both SSH keys and specify which key to use for each account.

**Cloning a Git Repository or Editing Remote URLs**

Now, you can use the correct SSH key when cloning your projects or editing remote URLs.

**Cloning for Your Personal Account:**

If you want to clone this repository using your personal GitHub account (zeron1g2k@gmail.com), you should use the following command:

```bash
git clone git@github.com-personal:kayafatix/Coursera.git
```

**Cloning for Your Company Account:**

If you want to clone this repository using your company account (fatih.kaya@emm-it.de), you should use the following command:

```bash
git clone git@github.com-company:Fatihkayaemm/internship.git
```

==========================================================

# Task-5
Certainly, here is the translation:

---

**Pushing Your Local Changes to the Company Repository on GitHub**

To push the changes you've made in your local repository to the remote repository (your company's repository on GitHub), you can follow these steps:

**1. Check Your Changes**

First, you can see which files have been changed by using the following command:

```bash
git status
```

This command shows which files have been modified and which ones haven't been committed yet.

**2. Stage the Changes**

To prepare the changes for committing, you need to stage the files:

- To stage all changes:

```bash
git add .
```

**3. Commit the Changes**

You can commit the changes with a message describing what you've done:

```bash
git commit -m "A message describing the changes you've made"
```

**4. Push to the Remote Repository**

To send the changes to the remote repository (the company repository), you'll use the `git push` command.

If you've correctly configured your `~/.ssh/config` file and have an SSH connection set up for your company account, you can push using the following command:

**Update the Remote Repository URL**

You should update the remote URLs for both GitHub repositories as follows:

- **For Personal Repository:**

```bash
git remote set-url origin git@github.com-personal:kayafatix/Coursera.git
```

- **For Company Repository:**

```bash
git remote set-url origin git@github.com-company:Fatihkayaemm/internship.git
```

Now, you can push your changes to both repositories with the correct SSH configuration:

```bash
git push origin main (or master)
```

=======================================================

# Task-6

Certainly! Here’s a step-by-step guide in English to create `develop` and `test` branches from your `master` branch:

---

### 1. Switch to the `master` Branch
Ensure you’re on the `master` branch:

```bash
git checkout master
```

### 2. Create the `develop` Branch
Create a new branch called `develop` and switch to it:

```bash
git checkout -b develop
```

### 3. Push the `develop` Branch to Remote
Push the newly created `develop` branch to the remote repository:

```bash
git push origin develop
```

### 4. Create the `test` Branch
Switch back to the `master` branch:

```bash
git checkout master
```

Create a new branch called `test` and switch to it:

```bash
git checkout -b test
```

### 5. Push the `test` Branch to Remote
Push the newly created `test` branch to the remote repository:

```bash
git push origin test
```
---

Now, you have both `develop` and `test` branches created and pushed to your remote repository!


===============================================================

# Task-8

If you’ve created branches on GitHub but haven’t yet synchronized them with your local repository, you can follow these steps to do so:

### 1. Fetch Existing Branches from the Remote Repository

First, you need to fetch the branches from the remote repository to your local repository:

```bash
git fetch origin
```

### 2. Track and Checkout the `develop` Branch

To start tracking the `develop` branch that you created on GitHub, use the following command:

```bash
git checkout -b develop origin/develop
```

This command creates a local `develop` branch and sets it to track the `develop` branch on GitHub.

### 3. Track and Checkout the `test` Branch

Similarly, for the `test` branch, use the following command:

```bash
git checkout -b test origin/test
```

This will create a local `test` branch and track the `test` branch on GitHub.

### 4. Add and Commit Files

Now that both branches are available locally, you can add files and commit them.

#### Add a File to the `develop` Branch:

```bash
git checkout develop
echo "This is a file on the develop branch." > develop.txt
git add develop.txt
git commit -m "Added develop.txt to the develop branch."
```

#### Add a File to the `test` Branch:

```bash
git checkout test
echo "This is a file on the test branch." > test.txt
git add test.txt
git commit -m "Added test.txt to the test branch."
```

### 5. Push Changes to the Remote Repository

Finally, you can push the changes in both branches to GitHub:

```bash
# Push the develop branch
git push origin develop

# Push the test branch
git push origin test
```

By completing these steps, you will have created the `develop` and `test` branches locally, added the respective files, and successfully pushed these changes to your GitHub repository.
========================  ================================

# Task 10/11
Here’s how to update the `test` branch with changes to the `ortak.txt` file, push those changes to the remote repository, and then merge the `test` branch into the `master` branch.

### 1. Edit the `ortak.txt` File on the `test` Branch

1. **Switch to the `test` Branch:**

   If you're not already on the `test` branch, switch to it:

   ```bash
   git checkout test
   ```

2. **Add Information to the First 5 Lines of `ortak.txt`:**

   Open `ortak.txt` in a text editor and add information to the first 5 lines. Alternatively, you can add the lines directly from the command line:

   ```bash
   echo -e "Line 1\nLine 2\nLine 3\nLine 4\nLine 5" >> ortak.txt
   ```

3. **Stage the Changes:**

   Stage the changes to be committed:

   ```bash
   git add ortak.txt
   ```

4. **Commit the Changes:**

   Commit the changes with a descriptive message:

   ```bash
   git commit -m "Added the first 5 lines of information to ortak.txt"
   ```

5. **Push the Changes to the Remote Repository:**

   Push the changes from the `test` branch to the remote repository:

   ```bash
   git push origin test
   ```

### 2. Switch to the `master` Branch and Merge `test` into `master`

1. **Switch to the `master` Branch:**

   To merge `test` into `master`, first switch to the `master` branch:

   ```bash
   git checkout master
   ```

2. **Merge `test` into `master`:**

   Now, merge the changes from the `test` branch into the `master` branch:

   ```bash
   git merge test
   ```

   This command merges the changes made in the `test` branch into the `master` branch. If there are no conflicts, the merge will complete successfully.

3. **(Optional) Push the Merged `master` Branch to the Remote Repository:**

   If you want to push the updated `master` branch to the remote repository:

   ```bash
   git push origin master
   ```

### Summary:
- Switch to the `test` branch and edit the first 5 lines of `ortak.txt`.
- Commit the changes and push them to the remote `test` branch.
- Switch to the `master` branch and merge the `test` branch into it.
- (Optional) Push the updated `master` branch to the remote repository.


======================================================

# Task-12

### Resolving Merge Conflicts Locally

1. **Perform the Merge and Encounter Conflicts**

   When you attempt to merge `develop` into `master`, if there are conflicts, Git will indicate this. Run the merge command:

   ```bash
   git merge develop
   ```

   If there are conflicts, Git will output a message similar to:

   ```
   CONFLICT (content): Merge conflict in ortak.txt
   Automatic merge failed; fix conflicts and then commit the result.
   ```

2. **Inspect the Conflicting Files**

   Git will mark the files with conflicts. Open the conflicting file(s) to view and resolve the conflicts. For example, if `ortak.txt` is conflicting:

   ```bash
   nano ortak.txt
   ```

   You will see conflict markers in the file like this:

   ```plaintext
   <<<<<<< HEAD
   This is the content from the master branch
   =======
   This is the content from the develop branch
   >>>>>>> develop
   ```

   - `<<<<<<< HEAD`: This section shows the changes from the current branch (`master`).
   - `=======`: This separates the changes from the two branches.
   - `>>>>>>> develop`: This section shows the changes from the branch being merged (`develop`).

   Resolve the conflict by editing the file to incorporate the changes as needed. You need to remove the conflict markers and adjust the content accordingly.

   For example:

   ```plaintext
   This is the resolved content that combines both branches.
   ```

3. **Stage the Resolved Files**

   After resolving conflicts, stage the resolved files using:

   ```bash
   git add ortak.txt
   ```

4. **Commit the Merge**

   Commit the resolved changes:

   ```bash
   git commit -m "Resolved merge conflicts"
   ```

### Summary

- **Merge**: Run `git merge develop` to start the merge process.
- **Resolve Conflicts**: Edit the files with conflicts, remove conflict markers, and adjust the content.
- **Stage**: Use `git add` to stage the resolved files.
- **Commit**: Use `git commit` to finalize the merge.

==========================================================
