# Drytide Labs Landing Page

This repository contains the static site for Drytide Labs. It is designed to be fully static, requiring no build steps, and can be deployed via multiple zero-configuration paths.

## Deployment

The site is configured to be deployable via two primary methods: GitHub Pages (zero-infra) and Docker/Nginx (self-hosted).

### Option 1: GitHub Pages (Zero-Infra)

The site is served directly from the `main` branch root. It is already pre-configured with a `CNAME` file pointing to `drytide.co`. 

To deploy:
1. Ensure GitHub Pages is enabled in the repository settings.
2. Set the source to the `main` branch and the `/ (root)` folder.
3. Push any changes to `main`. GitHub will automatically build and deploy the site.

### Option 2: Docker/Nginx (Self-Hosted)

For self-hosted environments or local testing, a `Dockerfile` and `docker-compose.yml` are provided. The stack uses `nginx:alpine` to serve the static assets directly without any runtime dependencies.

To deploy locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/drytidelabs/drytide-landing.git
   cd drytide-landing
   ```

2. Build and start the container in detached mode:
   ```bash
   docker compose up -d
   ```

3. The site will be available at `http://localhost:8080`.

To stop the container:
```bash
docker compose down
```

## Architecture

* **HTML/CSS Only:** No JavaScript frameworks, no Node.js, no build steps.
* **Brutalist Design:** Follows strict technical design constraints.
* **Responsive:** Mobile-first layout scaling via flexbox/grid.
