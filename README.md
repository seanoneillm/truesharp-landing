# TrueSharp Landing Page

## Deployment Instructions

This is a Next.js application that should be deployed to Vercel.

### Repository Setup

If you're deploying this to a separate repository (`truesharp-landing`), make sure all these files are at the **root level** of that repository, not in a subdirectory.

### File Structure

Your repository should look like this:

```
truesharp-landing/
├── app/
│   ├── api/
│   ├── components/
│   ├── globals.css
│   ├── layout.tsx
│   └── page.tsx
├── public/
├── package.json
├── next.config.js
├── tailwind.config.js
├── tsconfig.json
├── vercel.json
└── .env (create from .env.example)
```

### Environment Variables

Set up the following environment variable in Vercel:

```
BREVO_API_KEY=your_brevo_api_key_here
```

### Manual Fix for Current Error

The error "No Output Directory named 'public' found" suggests Vercel is treating this as a static site. To fix:

1. Make sure this is a **Next.js** project in Vercel settings
2. Ensure all files are at the repository root
3. The `public/` directory should exist (even if empty)

### Build Commands

- Build: `npm run build`
- Start: `npm start`
- Dev: `npm run dev`