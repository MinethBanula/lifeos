# LifeOS v1

A minimal life-coaching and planning surface built around four views: **Today, Week, Life, Rhythm**.

The main loop is: **talk → understand → suggest → plan → schedule → live → reflect → learn → repeat**.

## v1 workflow

1. Talk or voice-log naturally in ChatGPT.
2. ChatGPT outputs a Life Update JSON packet.
3. Drop that JSON anywhere in LifeOS, or use the small `import update` text action.
4. In **Week**, tick a task after you have time-blocked it in Google Calendar.
5. Use **Today** as the execution surface.
6. Reflect back in ChatGPT. The next packet can update tasks, focus areas, projects, habits, evidence, and coaching notes.

The app uses the Supabase project **LifeOS** with Row Level Security scoped to `auth.uid()`. It tries to create an anonymous authenticated session so the product can stay free of login forms. If Anonymous Sign-Ins are disabled in Supabase Auth, the app safely falls back to browser local storage.

Deployment is handled by GitHub Pages from `main`.