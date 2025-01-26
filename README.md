# GitHub

## **GitHub Quick Reference Guide**

### **Initial Setup**

**Creating a New Repository**  
1\. Go to github.com and sign in  
2\. Click "+" in top right corner → "New repository"  
3\. Name your repository  
4\. Choose visibility (public/private)  
5\. Don't initialize with README if you have an existing project

**First-Time Local Setup**  
Navigate to your project folder:

```bash

cd path/to/your/project

```

Initialize Git and push for the first time:

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/username/repository-name.git
git push -u origin main
```

**Setting Up SSH Authentication (Windows)**  
1\. Generate SSH key:

```bash
ssh-keygen -t ed25519 -C "your_github_email@example.com"
```

2\. **View your public key:**

```bash
type C:\Users\YourUsername\.ssh\id_ed25519.pub
```

**3. Add to GitHub:**  
\- Go to GitHub.com → Settings  
\- Click "SSH and GPG keys"  
\- Click "New SSH key"  
\- Paste your key  
\- Give it a title  
\- Click "Add SSH key"

**Regular Usage**

**Pushing New Changes**

**1. Add changed files:**

```bash
git add .
```

**2. Commit changes:**

```bash
git commit -m "Description of your changes"
```

**3. Push to GitHub:**

```bash
git push
```

**Optional: Setting Up Review Process**

**Configuring Branch Protection**  
1\. Go to repository on GitHub  
2\. Click Settings  
3\. Click Branches  
4\. Click "Add rule" under "Branch protection rules"  
5\. Type branch name (e.g., "main")  
6\. Configure desired rules:  
\- Require pull request reviews  
\- Set number of required approvals  
\- Require fresh approvals when new commits are pushed

**Working with Protected Branches**  
1\. Create new branch:

```bash
git checkout -b feature-name
```

2\. **Push changes:**

```bash
git add .
git commit -m "Feature description"
git push origin feature-name
```

3\. **Create Pull Request on GitHub**  
4\. **Wait for review/approval**  
5\. **Merge after approval**

##### **Common Issues**

**Permission Denied**  
If you see "Permission denied (publickey)":  
1\. Verify SSH key is properly generated  
2\. Ensure key is added to GitHub  
3\. Confirm you're using SSH URL for repository

**Branch Issues**  
If main/master branch confusion:

```bash
git branch -M main
```

##### **Working From Multiple Machines**

**Cloning to a New Machine**  
1\. Install Git on the new machine  
2\. Open terminal/command prompt  
3\. Navigate to where you want the project:

```bash
cd desired/location
```

**4. Clone the repository:**

```bash
git clone https://github.com/username/repository-name.git
```

5\. **Set up SSH keys on the new machine (follow SSH Authentication steps above)**

**Keeping Multiple Machines in Sync**  
Before starting work on any machine:

```bash
git pull
```

**After finishing work:**

```bash
git add .
git commit -m "Description of changes"
git push
```

**Collaborating with Others**

**Adding Collaborators to Private Repository**  
1\. Go to repository on GitHub  
2\. Click Settings  
3\. Click "Collaborators" in sidebar  
4\. Click "Add people"  
5\. Enter collaborator's GitHub username or email  
6\. They'll receive an invitation email

**Collaborator First-Time Setup**  
1\. Accept invitation from email  
2\. Clone repository:

```bash
git clone https://github.com/username/repository-name.git
```

##### 3. **Set up SSH keys on their machine**

**Collaboration Best Practices**  
\- Create branches for new features  
\- Use meaningful commit messages  
\- Communicate about who's working on what  
\- Pull before starting new work  
\- Consider using Issues for task tracking

**Best Practices**  
\- Write clear commit messages  
\- Commit frequently  
\- Pull before pushing  
\- Create meaningful branch names  
\- Keep repositories organized

####   
**\*Note: Replace placeholder values (username, repository-name, etc.) with your actual information when using commands.\***
