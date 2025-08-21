# GitHub-Powered CDN Manager

Advanced CDN solution using GitHub as storage backend with upload interface.

## Features
- Drag & drop file uploads
- GitHub repository as storage
- Custom CDN paths
- File type validation
- Progress indicators
- Render deployment ready

## Setup

1. Clone this repository
2. Create a new GitHub repository for assets
3. Generate GitHub PAT with `repo` scope
4. Set up environment variables (copy `.env.example` to `.env`)

## Deployment to Render

1. Create new Web Service
2. Connect your GitHub repository
3. Set environment variables:
   - `GITHUB_TOKEN`
   - `GITHUB_OWNER`
   - `GITHUB_REPO`
   - `CDN_DOMAIN`
4. Set build command: `npm install`
5. Set start command: `node server.js`

## CDN Configuration

1. Set up Cloudflare
2. Create CNAME record:
   - Name: `cdn`
   - Target: `your-render-service.onrender.com`
3. Add Page Rule for caching:
   - URL Pattern: `cdn.yourdomain.com/*`
   - Cache Level: Cache Everything
