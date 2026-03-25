# Data Forge Frontend Deployment Guide

## Environment Variables Setup

**For Development (.env):**
```
REACT_APP_BACKEND_URL=https://web-production-169b9.up.railway.app
```

**For Railway Production:**
1. Railway dashboard → Your project → Variables tab
2. Add: `REACT_APP_BACKEND_URL=https://web-production-169b9.up.railway.app`

## Build & Deploy
```bash
npm install
npm run build
# Deploy build folder to Railway
```

## Verification
- Console: `UPLOAD RESPONSE:` shows JSON with `summary`
- No HTML responses
- All API calls use dynamic backend URL

**No hardcoded localhost URLs found in codebase.**
**api.js uses strict process.env.REACT_APP_BACKEND_URL**
**Railway auto-injects REACT_APP_ vars during build.**

Project ready for production deployment.
