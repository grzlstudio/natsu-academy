# Natsu Academy — Phase 2 website upgrade

## What changed
- Preserves existing visual design and six Path previews.
- Adds Supabase email/password sign-in and sign-out.
- Requires authentication and a valid enrolment (or verified admin role) for learning routes.
- Adds email support contact.
- Removes localStorage-based demo completion toggles.
- Admin interface remains read-only/placeholder until secure server-side workflows are built.

## Connect your Supabase project
1. Open `config.js` in GitHub and edit the two placeholders.
2. Get Project URL from Supabase Project Settings → Data API / Connect.
3. Get **Publishable key** (`sb_publishable_...`) from Project Settings → API Keys.
4. Do NOT use the `sb_secret_...` key, database password or service role key.
5. Commit changes to `main`; Cloudflare Pages will deploy automatically.
6. Open `https://natsu-academy.pages.dev/#/login` and test your own admin sign-in.

## Important: database compatibility checks
The frontend expects `enrollments.user_id`, `enrollments.expires_at`, and optionally `enrollments.starts_at` and `enrollments.revoked_at`. Verify your actual SQL schema and adapt these field names if needed.

The existing `private.admin_users` record does **not** automatically populate `public.profiles.role`. To recognize an admin, the website currently reads `profiles.role='admin'` under RLS. Before using admin pages, establish a secure, database-controlled role synchronization mechanism or server-side role check. Do not allow users to update their own role.

If enrolments are denied by RLS or fields differ, access stays closed. This is intentional. Do not disable RLS to fix it.

## Not launch-ready
- Real paid lesson text/resources not authored or securely delivered.
- No payment confirmation or admin enrolment workflow yet.
- No robust backend authorization test suite or audit log.
- Progress saving is disabled until stable database lesson IDs are integrated.
- Supabase email delivery/password reset configuration should be tested before student invitations.
- CDN scripts require an internet connection; consider bundling dependencies for production.

This is an integration preview, not a production-ready paid course platform.
