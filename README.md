# ComfyGit Documentation

This repository hosts the GitHub Pages site for ComfyGit documentation at `docs.comfygit.org`.

## Structure

Documentation is deployed directly to root from the monorepo via GitHub Actions:
- **Source:** `comfygit-ai/comfygit` → `docs/comfygit-docs/`
- **Workflow:** `.github/workflows/publish-docs.yml`
- **Trigger:** Manual via GitHub Actions

## Custom Domain Setup

**Domain:** docs.comfygit.org

**DNS Configuration:**
- Type: CNAME
- Name: docs
- Target: comfygit-ai.github.io.
- TTL: 3600

**GitHub Pages Configuration:**
1. Repository Settings → Pages
2. Source: Deploy from branch `main` / `/ (root)`
3. Custom domain: `docs.comfygit.org`
4. Enforce HTTPS: Enabled

## Important Files

- **CNAME**: Must remain at root for custom domain to work
- **README.md**: This file (preserved during deployments)
- Everything else is auto-deployed from the monorepo

## Troubleshooting

### Site not updating
- Wait 1-2 minutes for GitHub Pages rebuild
- Check Actions tab in monorepo for build status
- Clear browser cache (Ctrl+Shift+R)

### Custom domain not working
- Verify DNS CNAME record: `dig docs.comfygit.org`
- Check GitHub Pages settings show custom domain

## Links

- **Live Site**: https://docs.comfygit.org
- **ComfyGit Repo**: https://github.com/comfygit-ai/comfygit
- **Organization**: https://github.com/comfygit-ai
