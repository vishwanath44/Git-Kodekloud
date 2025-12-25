## Day 1: Set Up Git Repository on Storage Server

Install Git on the Storage Server using yum

Create a bare Git repository at /opt/beta.git

## Step 1: Connect to the Storage Server

From your jumphost, SSH into the Storage Server. The exact command depends on how your environment is set up, but usually something like:
```bash
ssh <storage-server-username>@<storage-server-hostname-or-ip>
```
```bash
ssh natasha@ststor01
```
## Step 2: Install Git with yum
Once you’re on the Storage Server:

```bash
sudo yum install -y git
```
Verify installation:

```bash
git --version
```

## Step 3: Create the bare repository
Now initialize the repo exactly as required:

```bash
sudo git init --bare /opt/beta.git
```
Check the structure:

```bash
ls -la /opt/beta.git
```
You should see directories like branches, hooks, objects, refs.

## Step 4: Ownership (optional)
If the repo will be used by a specific user (e.g., thor), set ownership:

```bash
sudo chown -R thor:thor /opt/beta.git
```
If not, leaving it as root:root is fine for a basic setup.

## Step 5: Test clone
From any machine that can reach the Storage Server:

```bash
git clone <username>@<storage-server-ip>:/opt/beta.git
```
Or, if you’re still on the Storage Server and just want to test locally:

```bash
git clone /opt/beta.git ~/beta
```

## ✅ Task Completion Checklist

✔ Git installed using yum

✔ Bare repository created

✔ Repository path: /opt/beta.git

✔ Exact naming followed

## Test Lab Completed:

<img width="1691" height="960" alt="Screenshot 2025-12-25 104036" src="https://github.com/user-attachments/assets/bb6ba85f-9ae7-4205-93ee-caff27e37c31" />
