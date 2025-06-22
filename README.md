# Daily Commit Repository

This repository contains a GitHub Action workflow that runs daily and creates commits automatically.

## Workflow Details

- **Schedule**: Runs daily at 9:00 AM UTC
- **Purpose**: Demonstrates automated daily commits using GitHub Actions
- **Files**: Only the workflow file and daily log are tracked in this repository

## Files

- `.github/workflows/daily-commit.yml` - The GitHub Action workflow
- `daily-log.txt` - Log file updated by the workflow (created automatically)
- `.gitignore` - Excludes workspace files from being committed

## Manual Trigger

The workflow can also be triggered manually using the "workflow_dispatch" event in the GitHub Actions tab.

---

## **Directory and Script Usage**

The `app_ta` directory contains all the scripts and resources needed to build, test, and deploy the TDS Virtual TA application. Here is how to use them:

### **1. Scraping and Data Preparation**
- **Markdown Course Content:**
  - Use `app_ta/scrap/md_to_embeddings.py` to convert markdown files into embeddings for the course content.
- **Discourse Posts:**
  - Use `app_ta/scrap/scraper2.py` to scrape Discourse posts and save them as JSON.
  - Use `app_ta/scrap/create_embeddings.py` to convert the scraped JSON data into embeddings.

### **2. Embedding Files**
- All generated embedding files are stored in `app_ta/embeddings/`.

### **3. Running the API**
- The FastAPI application is located in `app_ta/app/`.
  - `main.py` is the entry point for the API.
  - `embeddings_util.py` contains LLM provider information.
  - `test_images/` contains images for testing image-based queries.

### **4. Evaluation**
- Use `app_ta/evaluate.yaml` for testing and evaluating the application.

--- 