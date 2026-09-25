# Smart Inventory

The UI and inventory workflows are now backed by Supabase instead of Firebase/localStorage.

## Supabase setup

1. Create a Supabase project.
2. Run `supabase-schema.sql` in Supabase SQL Editor.
3. In `supabase-config.js`, set the project URL and **anon/publishable** key from Project Settings → API. Never use a service-role key in browser code.
4. Enable Email provider in Authentication → Providers. If email confirmation is enabled, confirm the account before logging in.
5. Serve the app over HTTP (for example with VS Code Live Server or GitHub Pages).

The existing dashboard, reports, stock validation, sell/delete actions, history, and responsive UI remain intact. Row Level Security ensures every user can access only their own profile, inventory, and activity rows.
