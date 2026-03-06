# Derrick Weil Resume / Portfolio Site

This project is a curated Next.js site built from the provided source materials in this workspace. It emphasizes AI security, AI infrastructure, AI governance, and consulting credibility without inventing unsupported claims.

## Run

```bash
npm install
npm run dev
```

## Content Model

- Curated site content lives in `lib/site-data.ts`.
- The grounded Ask endpoint uses the pre-indexed `corpus` array in `lib/site-data.ts`.
- The `/admin` page exposes the content map, chatbot architecture summary, and maintenance notes required by the brief.

## Updating Content

1. Verify new facts against the exported source files before editing site content.
2. Add or update projects in `flagshipProjects` or `supportingProjects`.
3. Add short book excerpts to `writingThemes`.
4. Run `npm run reindex` after changing the corpus or writing excerpts.

## Chatbot Architecture

- Retrieval only over approved local source-derived excerpts.
- Refuses prompt extraction, source-boundary bypass, and fabricated claims.
- Input cap: 500 characters.
- Output cap: concise synthesis plus citations.
- Per-IP or session burst limit, daily limit, response cache, and temporary cooldown.

## Deployment Notes

- Keep secrets server-side only.
- Replace the placeholder sitemap domain in `app/sitemap.ts`.
- Add verified public contact details before production deployment.
