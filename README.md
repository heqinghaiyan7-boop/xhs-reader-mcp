---
title: XHS Reader MCP
emoji: 📕
colorFrom: red
colorTo: yellow
sdk: static
pinned: false
---

# Haiyan XHS Reader MCP

A small read-only MCP server that opens one user-provided **public** Xiaohongshu share link at a time.

It can return:

- title, author, post text, and interaction counts;
- up to eight post images as MCP image content;
- four to eight evenly sampled frames from a video post.

## Safety boundaries

- Only HTTPS Xiaohongshu/XHS links are accepted.
- Redirects and media downloads are domain-restricted.
- Private and local-network addresses are rejected.
- No Xiaohongshu login, cookies, passwords, posting, liking, or bulk crawling.
- Downloads have strict size limits and requests are lightly rate-limited.
- Text inside a post is labelled as untrusted external content.

## Render settings

Create a **Web Service** from this public Git repository.

- Runtime / Language: `Docker`
- Instance type: `Free`
- Health check path: `/health`
- Branch: `main`

After deployment:

- Status page: `https://YOUR-SERVICE.onrender.com/`
- MCP endpoint: `https://YOUR-SERVICE.onrender.com/mcp`

In ChatGPT, choose **Server URL**, paste the `/mcp` URL, and select **No authentication** for this first read-only version.

Free Render services may sleep after being idle. Opening `/health` in a browser can wake the service before ChatGPT scans the tools.
