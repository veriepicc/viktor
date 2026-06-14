# TinyTools — Project State

Live site: https://tinytools.store/ · Repo: veriepicc/viktor (public) · Host: GitHub Pages
Last updated: 2026-06-14

## Status: LIVE ✅

308 client-side tools + redesigned homepage, all deployed and serving over HTTPS at the custom domain.

### Hosting & Domain (DONE)
- GitHub Pages enabled from `main` / root.
- Custom domain tinytools.store, HTTPS enforced. Root `CNAME` file = tinytools.store.
- DNS at Namecheap: 4 A records → 185.199.108-111.153; CNAME www → veriepicc.github.io.
- Ignore the veriepicc.github.io/viktor path — custom domain serves the repo at the apex.

### Crawlability / SEO (DONE)
- robots.txt (allows all, points to sitemap).
- sitemap.xml with all 309 URLs (homepage + 308 tools).
- llms.txt at root.
- Canonical + robots(index,follow) + og:url on every page.

### Design system (DONE)
- Paper-and-ink editorial style. Tokens: bg #e8e6df, surface #f3f1ea, ink #16130f, muted #9c958a, accent vermilion #d6451f. Font Inter; mono meta labels (system mono). Lucide line icons.
- Homepage: left-aligned editorial hero ("Small, sharp tools for building on the web."), bordered stat panel, numbered "popular" index strip, mono ticker, hairline tool grid with icons. Search + category filters + all 308 tools intact.
- All 308 tool pages reskinned to the same system via a transform: stripped old stacked dark nav bars, reset palette (CSS vars for ~260 pages, hex-substitution for ~36 hardcoded-dark), flipped light/white text to ink by luminance, added one full-width fixed TinyTools bar (back arrow + wordmark + "Free tool" tag) + Lucide. Tool logic untouched.

### Deploy workflow
- Push directly to veriepicc/viktor main via GitHub API.
- For bulk changes use the git tree API = ONE commit for all files (avoids rate limits / many commits).

## TODO (not done yet)
1. Logo: AI-generate a mark (wrench/toolbox, vermilion #d6451f on paper #e8e6df, flat vector, no text, crisp at favicon size), then wire into nav + favicon. Currently using a Lucide "shapes" placeholder mark.
2. Google Search Console: verify tinytools.store, submit sitemap.xml, request indexing for homepage.
3. Traffic: post on Reddit (r/webdev, r/InternetIsBeautiful, r/SideProject), Dev.to article, X thread, dev Discords.
4. Adsterra: sign up once there's traffic (instant approval, no minimum), inject ad code across pages. NOT set up yet.

## Revenue notes
- Ad-supported (Adsterra) once traffic exists. Realistic: ~$0 months 1-3, $5-30/mo months 3-6, $50-200/mo months 6-12 with consistent SEO + posting.
- Big long-term numbers require a SaaS pivot, not ad-supported tool pages.

## Tech
- Every tool = standalone client-side HTML/CSS/JS, no backend.
- Category counts: Dev 95, Design 83, Utility 66, Text 32, Image 15, Network 14, AI 3.

## About the user (veriepic)
- 17, solo dev, Belgrade (UTC+2). GitHub: veriepicc.
- Strong modern C++ (C++20 modules). Other projects: Opus (from-scratch x64 systems language/compiler), Placebo (Minecraft Bedrock client).
- Prefers brutally honest feedback, casual tone, no flattery. Wants revenue fast.
