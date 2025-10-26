# Postman + Newman CI Sample Project

This project provides:
- A Postman collection with automated tests against JSONPlaceholder (>=8 tests total).
- A GitHub Actions workflow that runs Newman on pushes and PRs to main.
- A minimal OpenAPI `openapi.yaml` that you can use to publish docs.

Files:
- postman_collection.json
- postman_environment.json
- openapi.yaml
- .github/workflows/ci.yml
- package.json

How to use locally:
1. Install Node.js and Newman:
   npm install -g newman
2. Run tests:
   npm run test:newman
3. Test results will be saved to `newman-results/results.xml`.

How to enable CI:
1. Create a new GitHub repository and push all files.
2. Ensure branch `main` exists. On push or PR to main, GitHub Actions will run.

Publishing API documentation:
Option A - Postman Public Documentation
1. Import `postman_collection.json` into your Postman app.
2. Sign in to your Postman account and publish documentation from the collection via the Postman web view.
3. Postman will give you a public URL to share.

Option B - OpenAPI + Swagger UI
1. Use `openapi.yaml` with Swagger UI or ReDoc to display docs.
2. To host quickly, push to GitHub and enable GitHub Pages, or use any static hosting and show Swagger UI pointing to `/openapi.yaml`.

Submission checklist:
- After you push this repo to GitHub and run Actions, share:
  - GitHub Actions run link (from the workflow run page)
  - Public documentation link (from Postman or GitHub Pages)

Notes:
- This collection uses the public JSONPlaceholder API as a stable target.
- If you need the tests to target your own API, replace URLs in the collection with your endpoints.