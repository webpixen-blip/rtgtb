# Retail POS System - Deployment Guide

This folder contains a clean version of the POS system, optimized for deployment on Vercel and GitHub.

## Project Structure
- `/api`: Vercel serverless functions entry point.
- `/public`: Frontend assets (HTML, CSS, JS).
- `server.js`: Express application logic.
- `database.js`: MongoDB connection and schemas.

## Deployment Steps

### 1. GitHub Hosting
1.  Initialize Git (Already done by Antigravity).
2.  Create a new repository on GitHub (e.g., `retail-pos`).
3.  Link your local folder to GitHub:
    ```bash
    git remote add origin https://github.com/YOUR_USERNAME/retail-pos.git
    git branch -M main
    git push -u origin main
    ```

### 2. Vercel Hosting
1.  Go to [Vercel](https://vercel.com) and click **"New Project"**.
2.  Import your GitHub repository (`retail-pos`).
3.  **Environment Variables (CRITICAL)**:
    - Add a new variable named `MONGO_URI`.
    - Set the value to your MongoDB Connection String (e.g., `mongodb+srv://...`).
4.  Click **Deploy**.

## Local Development
To run this project locally, ensure you have Node.js installed and follow these steps:
1.  Install dependencies: `npm install`
2.  Set up your `.env` file with `MONGO_URI`.
3.  Start the server: `npm start`
