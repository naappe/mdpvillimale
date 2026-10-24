# MDP Villimalé
Standalone resident operations app. This is a separate repository and requires a separate Supabase project named `mdpvilimale`.

## Setup
1. Create the new Supabase Free project.
2. Run `schema.sql` **only on the new project's SQL Editor**.
3. Create the admin in Supabase Authentication (email: naappe@gmail.com). Insert their UUID into app_users as admin through SQL Editor.
4. Import authorized MDP residents using Supabase Table Editor. Never upload voter CSVs, ID documents, or photos to this public GitHub repository.
5. Replace placeholders in index.html with the **new project's** URL and publishable key (never a secret key).
6. Disable public self-signup in Supabase Auth; add staff users through the Auth dashboard and authorize them inside the app. Maximum three active staff.
7. Enable GitHub Pages from main / root.

## Access
Admin reads all records; staff see only assigned residents and may save only their own Vote Target, Voting Day and remarks. RLS protects database records. Original Vote database is unchanged. No real data loads until the new project is connected.