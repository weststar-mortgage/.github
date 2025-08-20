# 🚀 Starting a New .NET Project in Weststar Mortgage Org

This guide walks you through creating a new .NET application in our **weststar-mortgage** GitHub organization. Follow these steps whenever you need to start a new solution or repo.

---

## 1. Create a New Repository

1. Go to [weststar-mortgage GitHub Org](https://github.com/weststar-mortgage).
2. Click **New Repository**.
3. Name your repo (example: `loan-tracker`).
4. Set **visibility** to **Private**.
5. Initialize with:

   * **README.md** ✔
   * **No .gitignore here** (we’ll use our shared one instead)
6. Click **Create Repository**.

---

## 2. Clone the Repository

* **GitHub Desktop**

  1. Click **Code → Open with GitHub Desktop**.
  2. Choose a local folder (e.g., `C:\Dev\WeststarMortgage\loan-tracker`).

* **Visual Studio**

  1. Go to **File → Clone Repository**.
  2. Enter the repo URL.
  3. Choose a local folder.

---

## 3. Add the Standard `.gitignore`

We maintain a central `.gitignore` file for .NET applications in our org repo:
👉 [weststar-mortgage/.github/.gitignore](https://github.com/weststar-mortgage/.github/blob/main/.gitignore)

1. Copy that `.gitignore` into the **root** of your new repo.
2. Commit it as your **first commit**.

> ✅ This ensures local secrets (`appsettings.Local.json`) and build artifacts (`bin/`, `obj/`, `.vs/`) never end up in Git.

---

## 4. Create a New .NET Solution/Project

1. Open **Visual Studio**.
2. Go to **File → New → Project**.
3. Choose the project type (e.g., **ASP.NET Core Web API**).
4. Give the solution the **same name** as the repo.
5. Save it in the **cloned repo folder**.
6. Make sure **Place solution and project in the same directory** is checked.

---

## 5. Setup Configuration Files

We use `appsettings.json` plus environment-specific overrides.

* **Required files:**

  * `appsettings.json` → default config (non-sensitive values only).
  * `appsettings.Local.json` → local dev secrets (ignored in Git).
  * `appsettings.Development.json` → optional shared dev defaults.
  * `appsettings.Production.json` → only if needed (Azure App Settings usually cover this).

* **Example structure:**

```jsonc
// appsettings.json
{
  "Logging": {
    "LogLevel": {
      "Default": "Information"
    }
  },
  "ConnectionStrings": {
    "DefaultDb": ""
  }
}
```

```jsonc
// appsettings.Local.json (ignored in Git)
{
  "ConnectionStrings": {
    "DefaultDb": "Server=localhost;Database=MyDb;User Id=dev;Password=supersecret;"
  }
}
```

---

## 6. Local Development

* Run locally with Visual Studio (**F5** or **dotnet run**).
* Your app will load values from:

  * `appsettings.json`
  * `appsettings.Local.json` (your machine only)

---

## 7. Deployment to Azure

* Do **NOT** commit secrets into any config file.
* In **Azure App Service**:

  * Go to **Configuration → Application Settings**.
  * Add key/value pairs (they override `appsettings.json`).
  * These values are available at runtime via environment variables.

---

## 8. Adding Tailwind CSS (Optional, CDN-Only)

If you need Tailwind styles for UI, use the **CDN build**. No Node.js required.

```html
<!-- _Layout.cshtml or index.html -->
<link href="https://cdn.jsdelivr.net/npm/tailwindcss@3.4.1/dist/tailwind.min.css" rel="stylesheet">
```

---

## 9. Git Workflow Basics

Since many of us use **GitHub Desktop** or **Visual Studio Git Changes**, here’s the recommended flow:

1. **Create a branch** for your work (feature/fix).
2. Make your changes locally.
3. **Commit** often with clear messages.
4. **Push** your branch.
5. Open a **Pull Request (PR)** in GitHub.
6. Wait for review & approval.
7. **Merge** into `main`.

---

## 10. Checklist for New Projects

* [ ] Repo created in **weststar-mortgage** org.
* [ ] Central `.gitignore` copied from [.github](https://github.com/weststar-mortgage/.github).
* [ ] Solution/project created inside the repo folder.
* [ ] Config files setup (`appsettings.json` + local override).
* [ ] Local dev runs successfully.
* [ ] PR workflow followed.
* [ ] Azure secrets stored in App Service → Configuration.

---

💡 **Pro Tip:** When in doubt, ask before committing secrets. It’s easier to rotate passwords than to explain to security why you committed one.
