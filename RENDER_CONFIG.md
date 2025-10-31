# Render Deployment Configuration

This file helps Render understand how to deploy your backend.

## Render Configuration

When deploying to Render:
1. **Build Command**: `cd server && npm install`
2. **Start Command**: `cd server && npm start`
3. **Environment**: Node

## Environment Variables (Set in Render Dashboard)

- `MONGODB_URI`: Your MongoDB connection string
- `PORT`: Will be set automatically by Render
- `NODE_ENV`: `production`

## Health Check

Render will automatically check: `GET /api/health`

