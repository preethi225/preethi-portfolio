# 📋 DEPLOYMENT GUIDE — Step by Step
## Preethi Portfolio → Live on the Internet

---

## STEP 1 — Set Up MongoDB Atlas (Free Cloud Database)
**Time: ~10 minutes**

1. Go to: https://www.mongodb.com/atlas
2. Click "Try Free" → Create account
3. Choose FREE tier (M0 Sandbox)
4. Create a cluster → name it "portfolio"
5. Click "Database Access" → Add new user
   - Username: preethi
   - Password: (create one, SAVE IT)
6. Click "Network Access" → Add IP Address → Allow Access from Anywhere (0.0.0.0/0)
7. Click "Connect" → "Drivers" → Copy the connection string
   - Looks like: mongodb+srv://preethi:PASSWORD@cluster0.xxxxx.mongodb.net/
   - Replace <password> with your actual password
   - Add "portfolio_db" at end: .../portfolio_db?retryWrites=true&w=majority
8. SAVE THIS URI — you'll need it!

---

## STEP 2 — Push Code to GitHub
**Time: ~10 minutes**

1. Create NEW repository on GitHub
   - Name: preethi-portfolio
   - Set to PUBLIC ✅ (mentor must see it)
   - Do NOT initialize with README (we have one)

2. Open terminal/command prompt in your project folder:
```
git init
git add .
git commit -m "Initial commit - Preethi Portfolio"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/preethi-portfolio.git
git push -u origin main
```

3. Go to GitHub → your repo → Actions tab
   → You'll see the CI pipeline running automatically! ✅

---

## STEP 3 — Deploy on Render.com (Free Hosting)
**Time: ~10 minutes**

1. Go to: https://render.com → Sign up (use GitHub login)
2. Click "New +" → "Web Service"
3. Connect your GitHub repository (preethi-portfolio)
4. Fill in settings:
   - Name: preethi-portfolio
   - Environment: Node
   - Build Command: npm install
   - Start Command: npm start
5. Click "Environment Variables" → Add:
   - Key: MONGO_URI
   - Value: (paste your MongoDB Atlas URI from Step 1)
6. Click "Create Web Service"
7. Wait 2-3 minutes → Your site is LIVE! 🎉

Your URL will be: https://preethi-portfolio.onrender.com

---

## STEP 4 — Update README with Live URL

1. Open README.md in your project
2. Replace the live demo URL with your actual Render URL
3. git add README.md
4. git commit -m "Add live demo URL"
5. git push

---

## ✅ FINAL CHECKLIST (All 3 Credits)

[ ] Frontend — index.html (portfolio page) ✅
[ ] Backend — server.js (Node.js + Express) ✅
[ ] Database — MongoDB Atlas (cloud, not local) ✅
[ ] GitHub Repo — Public, mentor can view ✅
[ ] CI/CD Pipeline — GitHub Actions runs on every push ✅
[ ] Global Hosting — Render.com live URL ✅
[ ] README — Explains everything ✅
[ ] Workflow diagram — Local→Git→CI→Host→Browser ✅

---

## 🆘 If Render goes to sleep (free tier issue)

Free Render instances sleep after 15 minutes of inactivity.
Fix: Go to render.com → your service → Settings → turn off sleep
OR use https://uptimerobot.com (free) to ping your site every 5 min.
