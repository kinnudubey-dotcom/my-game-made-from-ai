# Deployment Instructions for Render

## Quick Deploy Steps

1. **Go to Render Dashboard**: https://dashboard.render.com
   - Sign in with GitHub

2. **Create New Static Site**:
   - Click "New +" button
   - Select "Static Site"

3. **Connect Repository**:
   - Choose "Connect GitHub"
   - Select repository: `my-game-made-from-ai`
   - Choose branch: `main`

4. **Configure Settings**:
   - **Name**: `dodge-game` (or any name you prefer)
   - **Branch**: `main`
   - **Root Directory**: (leave blank)
   - **Build Command**: (leave blank - no build needed)
   - **Publish Directory**: (leave blank)

5. **Optional Advanced Settings**:
   - Add a header rule:
     - Path: `/*`
     - Name: `Content-Type`
     - Value: `text/html`
   - Add rewrite rule:
     - Source: `/*`
     - Destination: `/game.html`

6. **Deploy**:
   - Click "Create Static Site"
   - Wait 1-2 minutes for deployment
   - Your game will be live at `https://[your-app-name].onrender.com`

## Alternative: Using render.yaml

Since we already have `render.yaml` configured, Render will automatically detect it when you connect the repository and apply the settings.

## Post-Deployment

Your game will be available at:
```
https://[your-chosen-name].onrender.com
```

The game supports:
- ✅ All gameplay features
- ✅ Sound effects (Web Audio API)
- ✅ Animations
- ✅ Multiple difficulty levels
- ✅ Pause menu
- ✅ Cutscenes

## Troubleshooting

- If the game doesn't load: Check that the rewrite rule is properly set
- If sounds don't work: Ensure you click on the page first (browser audio policy)
- If deployment fails: Check the render logs in the dashboard

