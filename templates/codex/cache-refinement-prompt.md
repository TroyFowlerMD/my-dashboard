# Cache Refinement Prompt

Codex prompt for refining caching and service-worker logic on static HTML/CSS/JS sites deployed via GitHub Pages.

---

You are a performance optimization expert. Review the following caching implementation and refine it for a static HTML/CSS/JS stack deployed via GitHub Pages:
1. Identify cache-busting strategies that work with service workers without breaking browser navigation.
2. Optimize the `Cache-Control` headers for assets.
3. Provide a fallback mechanism for when the user is offline, ensuring the core app remains functional.
4. Output a refined `service-worker.js` script that prioritizes the 'stale-while-revalidate' strategy for the site assets.
