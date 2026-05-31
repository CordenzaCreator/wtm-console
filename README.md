# WebToMobile Pro Posting Console

Mobile-friendly content review and posting interface for WebToMobile Pro.

Single-file static site hosted on GitHub Pages. Reads from the `wtm-posting-console` Supabase edge function on the WTM Supabase project (`dhriiwtpsaorqlxiuayu`). Daily generator `wtm-generate-manual-posts` fills the queue at 7 AM CT.

Platforms: LinkedIn, Instagram, TikTok, Facebook.

Workflow: Pull content. Post it. Mark done.

This repo is **separate from `gg-console`** by design. The two consoles point at different Supabase projects, different tables, and different edge functions. They do not share data.
