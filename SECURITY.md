# Security Policy

## Reporting a Vulnerability

Please report security issues privately to **net2outlawzz@gmail.com** with the subject `[SECURITY] biominute-shorts-studio`.

## Scope notes

- Never commit YouTube OAuth tokens, refresh tokens, or API keys.
- Keep `DATABASE_URL` and platform secrets in `.env` / Vercel only.
- Publishing pipeline should remain human-approved where possible (review before publish).
