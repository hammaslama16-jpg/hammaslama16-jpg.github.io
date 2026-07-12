# How to Deploy Everything

## 1. Portfolio Site (GitHub Pages)

### Steps:
1. Open GitHub.com → New repository
2. Name it: **hammaslama16-jpg.github.io** (exact name required)
3. Set it to **Public**
4. Upload `index.html` from this folder as the repo's root file
   - Or: clone the repo, copy `index.html` inside, commit & push
5. Go to Settings → Pages → Source: **Deploy from branch** → **main** → **/(root)**
6. Your site will be live at: **https://hammaslama16-jpg.github.io**

### Domain note:
You can also use a custom domain later (Settings → Pages → Custom domain)

---

## 2. Supabase Setup (for contact form)

### Steps:
1. Go to: https://supabase.com/dashboard/project/ynrwbezrioihpusfnzfw
2. Log in with: hammaslama16@gmail.com
3. Open **SQL Editor** (left sidebar)
4. Paste the contents of `supabase-setup.sql`
5. Click **Run**

### Get your anon key:
1. Go to **Project Settings** → **API**
2. Copy the **anon public** key (starts with `eyJ...`)
3. Open `index.html` and find this line:
   ```js
   const SUPABASE_ANON_KEY = 'YOUR_SUPABASE_ANON_KEY_HERE';
   ```
4. Replace it with your actual anon key:
   ```js
   const SUPABASE_ANON_KEY = 'eyJ...your-actual-key...';
   ```
5. Re-upload `index.html` to GitHub (commit & push)

### Test it:
Submit a message on your portfolio site → it saves to the `contacts` table.
View entries at: Supabase → Table Editor → `contacts`

---

## 3. Contra Profile

Copy the content from `contra-profile.md` into:
- Contra → Edit Profile → Bio, Services, Pricing

Set your initial rate: **$30/hr or $200/project** (increase after 2-3 reviews)

---

## 4. Superset Bounties

Follow `bounties-report.md` step by step.
Start with the survey + Slack join this week.

---

## Files in This Folder

| File | Purpose |
|------|---------|
| `index.html` | Portfolio website (GitHub Pages ready) |
| `supabase-setup.sql` | SQL to create contacts table |
| `contra-profile.md` | Profile copy for Contra |
| `bounties-report.md` | GitHub bounty opportunities |
| `deploy-instructions.md` | This file |
