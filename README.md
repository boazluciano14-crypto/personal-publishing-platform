@tailwind base;
@tailwind components;
@tailwind utilities;

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen',
    'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue',
    sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.line-clamp-3 {
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
}
{
  "name": "personal-publishing-platform",
  "version": "1.0.0",
  "description": "Personal publishing platform with ads and notifications",
  "main": "index.js",
  "scripts": {
    "dev": "concurrently \"npm run dev -w frontend\" \"npm run dev -w backend\"",
    "build": "npm run build -w frontend && npm run build -w backend",
    "start": "npm start -w backend",
    "install-all": "npm install && npm install -w frontend && npm install -w backend"
  },
  "workspaces": [
    "frontend",
    "backend"
  ],
  "devDependencies": {
    "concurrently": "^7.6.0"
  },
  "keywords": ["publishing", "stories", "poems", "ads", "notifications"],
  "author": "boazluciano14-crypto",
  "license": "MIT"
}
{
  "name": "frontend",
  "version": "1.0.0",
  "private": true,
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "next lint"
  },
  "dependencies": {
    "next": "^14.0.0",
    "react": "^18.0.0",
    "react-dom": "^18.0.0",
    "axios": "^1.6.0",
    "socket.io-client": "^4.5.0",
    "tailwindcss": "^3.3.0"
  },
  "devDependencies": {
    "postcss": "^8.4.0",
    "autoprefixer": "^10.4.0"
  }
}
/** @type {import('next').NextConfig} */
const nextConfig = {
  reactStrictMode: true,
  images: {
    unoptimized: true,
  },
}

module.exports = nextConfig
