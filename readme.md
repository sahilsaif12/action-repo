# 📦 action-repo

## 🌟 Purpose

`action-repo` is a demo GitHub repository created as part of a developer assignment to **simulate GitHub events (Push, Pull Request, Merge)** for webhook testing.

The repository is intentionally designed to:
- Trigger real GitHub webhooks on key actions.
- Send those webhooks to a receiver service (hosted separately in the `webhook-repo`).
- Help test, capture, and process GitHub events for learning and assessment purposes.

👉 **This is NOT a spam or malicious repository.**  
👉 It exists solely to test webhook event flows end-to-end.

---

## 🚀 What is this repository used for?

✅ **Triggering GitHub webhooks**  
When actions like:
- pushing commits
- creating or updating pull requests
- merging PRs  
are performed on this repo → GitHub sends webhook events to the configured endpoint.

✅ **Supporting a webhook receiver**  
These events are received by the `webhook-repo` (a Flask server), which:
- captures and logs events
- stores them in MongoDB
- provides them to a frontend UI for display

---

## 🔗 How is this repository used?

1️⃣ The repo is connected to a webhook URL (e.g., via GitHub Webhooks settings).  
2️⃣ Developer performs actions in this repo:
- `git push`
- create/update PR
- merge PR  
3️⃣ GitHub sends event payloads to the webhook receiver.
4️⃣ The receiver processes and stores the data for display.

---

## 🛠 Technologies involved

- **GitHub Webhooks** (sending event data)
- **Flask (Python)** (in the webhook-repo to capture events)
- **MongoDB** (storing the event logs)
- **React + Vite** frontend (polls and displays event logs)

---

## ⚠️ Important notes

- This repository is **not meant for production applications**.
- It contains minimal code or content because its sole purpose is to generate GitHub actions for webhook testing.
- There is no sensitive data, malware, or spam in this repository.
- The commit messages, branches, and PRs may appear artificial as they are created purely for testing the webhook flows.

---

## ✨ Related repositories

➡ [`webhook-repo`](https://github.com/your-username/webhook-repo)  
Captures and processes webhooks sent from this repository. And this is the main repo

---

## 🙏 Acknowledgements

This repo was created as part of a developer assessment :
- GitHub webhook integration
- backend processing of GitHub events
- frontend polling and display of event logs

