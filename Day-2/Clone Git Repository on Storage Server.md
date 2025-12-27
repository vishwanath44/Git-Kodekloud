## Day 2: Clone Git Repository on Storage Server

## Task Summary

Source repository: /opt/apps.git

Destination directory: /usr/src/kodekloudrepos

User to perform task: natasha

🔹 Step-by-Step Instructions
Step 1: Switch to the natasha user
```bash
ssh natasha@ststor01
```
Ensure you are operating as the correct user.
```bash
sudo su - natasha
```

Verify:
```bash
whoami
```

Output should be:

natasha

Step 2: Verify Git is available

Check if Git is installed (do not install unless explicitly required).
```bash
git --version
```
Step 3: Check if destination directory exists

⚠️ Do not create or modify directories unless they already exist.
```bash
ls -ld /usr/src/kodekloudrepos
```

If the directory exists → proceed

If it does not exist → stop and inform the administrator (do not create it)

Step 4: Navigate to the destination directory
```bash
cd /usr/src/kodekloudrepos
```
Step 5: Clone the repository

Clone the repository without making any changes.
```bash
git clone /opt/apps.git
```
Step 6: Verify the clone

Confirm the repository was cloned successfully.
```bash
ls
```

(Optional)
```bash
cd apps
```
```bash
git status
```

Expected output:

On branch main
nothing to commit, working tree clean

## ✅ Task Completion Checklist

✔ Repository cloned from /opt/apps.git

✔ Cloned into /usr/src/kodekloudrepos

✔ Performed using natasha user

✔ No permissions or files modified

Task Screenshot:

<img width="1730" height="883" alt="Screenshot 2025-12-27 103445" src="https://github.com/user-attachments/assets/da496ffb-9ef7-49e8-bc54-b5e97d57cca9" />
