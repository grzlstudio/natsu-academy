# Natsu Academy — Phase 1 frontend starter

An elegant, responsive **public prototype** for Natsu Academy, designed for GitHub + Cloudflare Pages.

## What works now
- Responsive public homepage and course overview
- Six learning Paths with sample lesson pages
- Student dashboard preview and browser-local sample progress tracking
- Practice Desk with a sample multiple-choice Quick Check
- Resources, account, login and admin **design previews**
- Brand palette: `#FFF6F8`, `#F6C8D7`, `#EC80AE`, `#D58FA5`, `#65434D`

## What is NOT implemented
**This is not yet a paid-course platform.** There is no real authentication, payment processing, purchase verification, secure file storage, database, access expiry, admin permissions, enrolment, or complete course curriculum. The demo dashboard and admin page are publicly viewable; demo progress is saved in browser localStorage. Do **not** upload private student data or paid lesson files to this project. Do **not** advertise it as a complete course yet.

## Preview locally
Open `index.html` in a browser. No install or build tools required.

## Publish to GitHub and Cloudflare Pages
1. Create a new GitHub repository, e.g. `natsu-academy`. Keep it separate from the existing GRZL Studio repository.
2. Upload **index.html**, **styles.css**, **app.js**, and **README.md** to the repository root.
3. In Cloudflare, create a new **Pages** project and connect the new GitHub repository.
4. Select **no framework / None** (static HTML site), **no build command**, and set the **build output directory** to `/` (repository root) if the UI requires one. Cloudflare UI wording can vary.
5. Deploy and test the assigned `*.pages.dev` address on desktop and mobile.
6. After owning and configuring `grzlstudio.com` in Cloudflare, add `academy.grzlstudio.com` as a Pages custom domain. This requires domain/DNS control; the subdomain is not automatically live.

## Production roadmap
1. Implement a real authentication provider (e.g. Supabase Auth) and secure server-side enrolment checks.
2. Create protected student/admin roles with database row-level security; never trust client-side route hiding.
3. Store lesson resources privately with expiring authenticated download links.
4. Build purchase request/verification, admin approval and 6-month access expiry rules.
5. Replace placeholder lessons with complete authored content and actual downloadable templates.
6. Test abuse cases, expired enrolments, revoked access, mobile accessibility, backups and privacy notices.

## Proposed offer
Social Media Management Starter Course — provisional ₱499 one-time payment, 6 months access, optional 7-day suggested learning journey. Six Paths, with lessons, Practice Desk and Quick Checks. No guarantee of job placement or mastery in seven days.
