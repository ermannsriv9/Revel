# What is an API Key?

An **API key** is a unique identifier used to authenticate requests made to an API (Application Programming Interface). It's like a password or token that grants access to a particular service or resource.

### Key Uses of an API Key:

1. **Authentication and Authorization:**  
   The API key ensures that the user making the request has the necessary permissions to access the service. It helps authenticate the client or user making requests to the API, ensuring that only authorized users can interact with the service.

2. **Access Control:**  
   API providers can control who has access to the resources, manage usage limits, and monitor activity. It helps restrict or allow access to specific users, based on the key associated with the request.

---

#  How to Generate API Keys for BigQuery & Gemini in GCP

Follow these steps to generate an API key for services like **BigQuery** and **Gemini** in Google Cloud Platform:

### Step 1: Sign in to Google Cloud Console
- Go to [Google Cloud Console](https://console.cloud.google.com/).
- Log in with your Google account.

### Step 2: Create a Project
- In the Cloud Console, click the **project drop-down** on the top-left.
- Select **New Project**.
- Name your project and click **Create**.

### Step 3: Enable Required APIs
- Navigate to **API & Services > Library**.
- Search for:
  - **BigQuery API**
  - **Gemini API**
- Click each and enable them for your project.

### Step 4: Create an API Key
- Go to **API & Services > Credentials**.
- Click **Create Credentials** → **API Key**.
- Copy the key displayed.

### Step 5: Restrict the API Key (Optional but Recommended)
- Click **Restrict Key**.
- Choose restrictions like:
  - Specific APIs (e.g., BigQuery)
  - IP address restrictions

### Step 6: Save Your API Key Securely
- Store your API key in an environment variable or secret manager.
- **Never expose it in public code repositories.**

---

# 🧰 Git Setup & GitHub Integration

Steps to install Git, configure it, set up GitHub, and push code to a repository.

### Step 1: Download & Install Git
- Visit: [https://git-scm.com/download/win](https://git-scm.com/download/win)
- Download Git for Windows installer.
- During installation:
  - Enable **"Git Bash Here"**
  - Choose **"Use Git from Git Bash only"**
  - Set **VS Code** as the default editor

### Step 2: Configure Git
Open **Git Bash** and run:
```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
git config --global --list  # optional check
```

### Step 3: Create a GitHub Account
- Visit [https://github.com](https://github.com)
- Sign up if you don’t have an account

### Step 4: Generate GitHub Token (Classic)
- Navigate to:
  `Settings > Developer Settings > Personal Access Tokens > Tokens (classic)`
- Click **Generate new token**
- Select scopes like:
  - `repo`, `workflow`, `read:org`, etc.
- Copy and store the token securely

### Step 5: Clone a GitHub Repository
```bash
git clone https://github.com/ermannsriv9/Revil.git
cd Revil
```

### Step 6: Check Git Status
```bash
git status
```

### Step 7: Initialize & Push Project to GitHub
```bash
echo "# Revel" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ermannsriv9/Revel.git
git push -u origin main
```

### Step 8: Sync Branch & Add Files
```bash
git pull origin main
git checkout main
# Add or update your documentation

git add filename
git commit -m "document for API key and Git setup"
git push origin main
```

