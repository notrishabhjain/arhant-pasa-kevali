# Arhant Pāsā Kevalī

A mobile-friendly web app for the Jain dice oracle *Arhant Pāsā Kevalī* (pages 445–461 of the printed book, composed by Shri Pandit Vrindavan ji of Kashi).

It walks through the book's method step by step: introduction, preparation, the invocation couplets, meditation, the three mantras (or the Ṇamokār Mantra), three throws of the four-sided die (अ, र, हं, त), and the result for the letters thrown. Every screen is available in Hindi and English.

- **Hindi** text is the book's printed text, word for word. **English** is a close translation, with the original Hindi one tap away.
- Four combinations (र-र-त, र-हं-अ, र-हं-र, र-हं-हं) are not printed on the source pages, and the app says so instead of inventing a result.
- Each throw uses the browser's cryptographic random generator (`crypto.getRandomValues`) with rejection sampling, so all four letters are exactly equally likely.

## Deploy

It is a single static `index.html` with no build step. On Vercel, import this repository with the framework preset **Other** and no build command; `vercel.json` adds a few response headers.
