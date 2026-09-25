# HealthChrono-Web

Official marketing website, legal compliance hub, and support portal for **HealthChrono** ([https://gethealthchrono.com](https://gethealthchrono.com)).

## Architecture & Technology Stack

- **Framework:** [Astro 5](https://astro.build/)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/)
- **Deployment Adapter:** [`@astrojs/netlify`](https://docs.astro.build/en/guides/integrations-guide/netlify/)
- **Hosting & CDN:** Netlify (`healthchrono-web` project under team `Dr IT - The IT Ninjas`)
- **DNS & CDN Edge:** Cloudflare (`gethealthchrono.com`)
- **Support Backend:** Netlify Forms routed automatically to `info@drit.ninja`

## Routes & Pages

| Route | Purpose | Compliance Standards |
|---|---|---|
| `/` | Landing page, hero, feature breakdown, interactive mobile gallery, FAQ | Marketing, App Store & Google Play badges |
| `/privacy` | Full Privacy Policy | GDPR, CCPA/CPRA, FTC Health Breach Rule, Washington My Health My Data |
| `/terms` | Terms of Service & Medical Disclaimer | Informational tracking terms, App Store subscription terms |
| `/support` | Customer support ticket form & contact info | Netlify Forms enabled, forwarded to `info@drit.ninja` |
| `/support-success` | Confirmation screen after submitting support ticket | User confirmation & expectations |
| `/delete-data` | Account & Data Deletion Portal | Google Play Data Safety & Apple Account Deletion compliance |
| `/404` | Custom branded error page | Fallback navigation |

## Local Development

```bash
# Install dependencies
npm install

# Start local Astro dev server
npm run dev

# Build for production
npm run build

# Preview production build locally
npm run preview
```

## Deployment & DNS Configuration

- **Production Branch:** `main`
- **Integration Branch:** `dev`
- **Custom Domains:**
  - `gethealthchrono.com` (Apex) -> Cloudflare `A` record pointing to Netlify Load Balancer `75.2.60.5` (DNS only)
  - `www.gethealthchrono.com` -> Cloudflare `CNAME` record pointing to `healthchrono-web.netlify.app` (DNS only)
- **Clerk Authentication Records:** Preserved on Cloudflare for mobile app backend auth (`accounts`, `clerk`, `clk2._domainkey`, `clk._domainkey`, `clkmail`).
