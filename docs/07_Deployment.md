# 📌 Deployment Plan

##  🔹 Frontend Deployment (Phase 1)
1. **Build Process**
   - Use the build script provided by Vite:
     ```bash
     npm run build
     ```
2. **Deploy on GitHub Pages**
   - Install gh‑pages:
     ```bash
     npm install gh-pages --save-dev
     ```
   - Add the following to your `package.json`:
     ```json
     "homepage": "https://yourusername.github.io/tms",
     "scripts": {
       "predeploy": "npm run build",
       "deploy": "gh-pages -d dist"
     }
     ```
   - Run:
     ```bash
     npm run deploy
     ```

##  🔹 Future (Phase 2)
- After backend integration, update deployment scripts and consider using platforms like Vercel or Netlify for full‑stack deployment.
- Optionally integrate CI/CD with GitHub Actions for automated testing and deployment.
