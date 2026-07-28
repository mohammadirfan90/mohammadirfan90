# Guide: Deploying Your Premium GitHub Profile README

This guide walks you through customizing your profile information, setting up the automated **Contribution Snake Game**, and deploying the README to GitHub.

---

## 🛠️ Step 1: Customize Your Information

Open [README.md](README.md) in your editor (e.g., VS Code) and update the following details to match your current URLs:

1. **Portfolio URL Placeholder:**
   * Find `https://your-portfolio.dev` in the file.
   * Replace it with your actual personal portfolio URL.
2. **Phone Number:**
   * Find `+8801400748802` (in text and in the badges section `tel:+8801400748802` / `Phone-%2B8801400748802-blue`).
   * Update it if your number changes.

---

## 🚀 Step 2: Push to GitHub

To make this your official GitHub profile page:

1. **Create a Special Repository:**
   * Go to [GitHub - New Repository](https://github.com/new).
   * Name the repository **exactly** your username: `mohammadirfan90`.
   * **Crucial:** Make sure the repository is **Public** and check the box to initialize it (or leave it blank to push these files).
2. **Initialize Git and Push:**
   * Open a terminal inside the `f:\Job Prep` folder.
   * Run the following commands:
     ```bash
     git init
     git add .
     git commit -m "feat: initial premium profile readme setup"
     git branch -M main
     git remote add origin https://github.com/mohammadirfan90/mohammadirfan90.git
     git push -u origin main --force
     ```

---

## 🐍 Step 3: Setup the Contribution Snake Game

The contribution graph animation is powered by a GitHub Action workflow which runs automatically once a day, or whenever you push updates.

We have already created the workflow file for you at [generate-snake.yml](.github/workflows/generate-snake.yml). Here is how to activate it:

1. **Enable Write Permissions for GitHub Actions:**
   * Go to your repository on GitHub: `https://github.com/mohammadirfan90/mohammadirfan90`.
   * Click on **Settings** (top tabs) -> **Actions** (under Code and automation) -> **General**.
   * Scroll down to **Workflow permissions**.
   * Select **Read and write permissions** and click **Save**.
2. **Run the Action Manually (First Time):**
   * Go to the **Actions** tab in your GitHub repository.
   * Under the left sidebar, click on the workflow named **Generate Snake**.
   * Click the **Run workflow** dropdown on the right side and click the green **Run workflow** button.
   * Once it runs successfully (takes about 30 seconds), it will create a new branch named `output` and upload the SVGs there.
3. **Verify:**
   * Go back to your GitHub profile: `https://github.com/mohammadirfan90`.
   * You should see the animated snake eating your contribution dots at the bottom of the page!
