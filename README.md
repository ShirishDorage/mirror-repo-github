# Repository mirroring (from GitLab to GitHub)

 This project demonstrates how to **automatically sync a GitLab repository with GitHub**, ensuring both repositories stay updated in real time.

 ---
 ##  Overview

Repository mirroring allows you to **keep two repositories synchronized** — for example, pushing code from **GitLab** to **GitHub** automatically whenever changes are made.

This is useful for:
- Backing up your GitLab repository to GitHub
- Collaborating across different platforms
- Maintaining public and private copies of the same project

---
### Step-1: Create Repository in GitLab
Create a Blank repository with README.md file
![](./images/Screenshot%202025-10-13%20223330.png)

### Step-2: Create Repository in GitHub
Create a repository with README.md file
![](./images/Screenshot%202025-10-14%20234216.png)

### Step-3: Create Personal Access Token(classic)
* GitHub → **Settings → Developer settings → Personal access tokens → Generate new token**
* Grant all permissions/Scopes

**Copy the token**
![](./images/Screenshot%202025-10-14%20170956.png)

### Step-4: Create a mirroring Repository
Set up your project to automatically push or pull changes to/from another repository. Branches, tags, and commits will be synced automatically.

* Open your project → **Settings → Repository → Mirroring repositories**.
* Click ** mirror repository**.
* For **Git repository URL** use the HTTPS push URL in this form:
```
https://<GITHUB_USERNAME>@github.com/<GITHUB_USERNAME>/<GITHUB_REPO>.git
```
* When prompted for a password, paste the **GitHub access token** and save

![](./images/Screenshot%202025-10-14%20235206.png)

### Step-5: Clone GitLab Repository in your machine, add files and push to server 

* Open git bash and Clone repository
```
git clone https://gitlab.com/shirishdorage9696/mirror-repo-gitlab.git
```
* cd to repository
```
cd <REPO_NAME>
```
* Create a file(index.html)
```
nano index.html
```
* Add some lines
```
<h1>This is my index page for mirroring project</h1>
```
* **commit** and **push** to GitLab Server
```
git add index.html
git commit -m "message"
git push -u origin main
```
## Output
**In GITLAB:**
![](./images/Screenshot%202025-10-10%20083657.png)

**In GITHUB:**

Automatically index.html file is synchronized to GitHub repository.
![](./images/Screenshot%202025-10-14%20235906.png)

## Conclusion
By setting up repository mirroring between GitLab and GitHub, you can effortlessly keep your code synchronized across both platforms.

This ensures smooth collaboration, reliable backups, and easy access for your team.

With GitLab’s automated push mirroring feature, your updates are securely and continuously reflected on GitHub — saving time, reducing manual work, and keeping your projects consistently up to date.

