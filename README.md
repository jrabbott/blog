# Personal Blog

This repository contains the source code and content for my personal blog, built with **Hugo** and deployed using **GitHub Pages**.

The blog is a space where I write about projects, ideas, and things I’m learning, while also serving as a playground for experimenting with static site workflows.

Visit the live site here:
👉 https://jrabbott.github.io/blog

## 🚀 Tech Stack

* **Hugo** – Static site generator
* **GitHub Pages** – Hosting and deployment
* **Markdown** – Content authoring

## 📁 Project Structure

```text
.
├── archetypes/    # Content templates
├── content/       # Blog posts and pages
├── layouts/       # Custom layouts and templates
├── static/        # Static assets (images, files, etc.)
├── themes/        # Hugo themes
├── config.toml    # Site configuration
└── README.md
```

## 🛠 Local Development

To run the site locally:

1. Install Hugo
2. Clone this repository
3. Start the development server:

```bash
hugo server
```

The site will be available at `http://localhost:1313` with live reload enabled.

## 🌍 Deployment

The site is automatically deployed to **GitHub Pages** from this repository. Pushing changes to the main branch updates the live site.

## ✍️ Writing Posts

New posts can be created with:

```bash
hugo new posts/my-post-title.md
```

Content is written in Markdown and stored in the `content/` directory.

## 📌 Notes

* This repo is intentionally simple and evolving.
* Structure, theme, and tooling may change over time as the blog grows.
