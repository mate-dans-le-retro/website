# Mate Dans Le Rétro... Gaming - Official Website

Official website for **Mate Dans Le Rétro... Gaming**, an association of
nostalgic 40-something geeks organizing retro gaming events.

## About

Mate Dans Le Rétro... Gaming is a French association that brings together
nostalgic gamers for retro gaming events.

The major events takes place at [La Caserne](https://lacaserne-sourcieux.fr/) in
Sourcieux-les-Mines around the All Saints' Day.

The event features:

- Arcade machines and 20+ consoles from the 80s to early 2000s
- Free access gaming sessions
- Tournaments and competitions
- A weekend full of nostalgia for Sega, Nintendo, Atari 2600, and PlayStation
  fans

## Features

- 📱 **Responsive Design**: Mobile-first approach with Tailwind CSS
- 🎨 **Custom Styling**: Retro gaming-inspired color scheme (purple & pink)
- 🔍 **SEO Optimized**: Meta tags, Open Graph, and Twitter Cards
- 🖼️ **Progressive Images**: Optimized thumbnails and hero images
- ⚡ **Fast Loading**: Minimal dependencies, optimized assets
- 🎮 **Retro Aesthetics**: Gaming-inspired fonts and decorative elements

## Contact & Social

- **Instagram**: [@mate_dans_le_retro](https://www.instagram.com/mate_dans_le_retro/)
- **Website**: [www.matedansleretro.fr](https://www.matedansleretro.fr)

## Contributing

### Tech Stack

This is a simple, modern static website built with:

- **HTML5** with semantic markup
- **CSS3** with custom styling
- **Tailwind CSS** for utility-first styling
- **Google Fonts** (Montserrat)
- Responsive design with mobile-first approach

### Deployment

The website is automatically deployed on
**[Vercel](https://vercel.com/mate-dans-le-retro)** when new code is pushed in
the GitHub repository

### Branches

- **`main`** - Preview environment _(staging/preprod)_

  - Automatically deploys to preview URL:
    [preview.matedansleretro.fr/](http://preview.matedansleretro.fr/)
  - Used for testing and review

- **`prod`** - Production environment
  - Automatically deploys to main domain:
    [www.matedansleretro.fr](https://www.matedansleretro.fr) or
    [matedansleretro.fr](https://matedansleretro.fr)
  - Stable, live version

### Development

It is recommended that you use Prettier and ESLint extensions in your IDE to
have proper formatting and code conventions.

> However no conventions are enforced in this repository for the moment.

#### Prerequisites

- Any modern web browser
- (Optional, for easier local development) A local web server (if you are using VSCode
  alike IDE, you can use the
  [Live Server extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
  that support auto-refresh,
  or you can start a simple Python HTTP Server, see below)

> Note that as it's only a simple HTML page, you can also directly open the
> index.html file to see your changes (but you'll have to refresh it manually)

#### Local Development

1. Clone the repository:

```bash
git clone git@github.com:mate-dans-le-retro/website.git
cd website
```

or using HTTPS:

```bash
git clone [git@github.com:mate-dans-le-retro/website.git](https://github.com/mate-dans-le-retro/website.git)
cd website
```

2. Open the page:

```bash
# Option 1: Direct file access
open index.html

# Option 2: Local server (example using simple Python HTTP Server) and visit
# "http://localhost:8000"
python -m http.server 8000
```

### File Structure

```plain
.
├── index.html              # Main HTML file
├── styles.css              # Custom CSS styles
├── tailwind.config.js      # Tailwind CSS configuration
├── images/                 # Images and graphics
│   ├── logo.png
│   ├── bg_hero.png
│   └── thumbnails/
├── favicon files           # Various favicon formats
└── site.webmanifest       # PWA manifest
```

### Deployment Process

> For branch naming and commit guidelines and convention, see the
> [contributing doc](./CONTRIBUTING.md)

#### Standard workflow

1. Create a new branch from `main`:
   `git checkout main && git pull && git checkout -b my-branch`
2. Write your code and push it to your branch
3. Create a PR to `main`
4. Vercel automatically builds and deploys your PR on a dedicated environment
   _(URL will be available in your PR)_ on each push
5. Check your changes in this dedicated environment
6. Once tested and approved, merge your PR into `main` **(using squash commit)**
7. Vercel automatically builds and deploys the `main` branch to
   [the preprod environment](http://preview.matedansleretro.fr/) on each push on
   `main`
8. For double safety, check your changes on
   [the preprod](http://preview.matedansleretro.fr/)
9. Once tested and approved, create a PR from `main` into `prod` and merge it
   **(using merge commit)**

> You could also manually merge `main` into `prod` using Git:
> `git checkout prod && git pull && git merge origin/main && git push`
> Note though that
> **creating a PR is recommended to have proper history and traceability**

10. Vercel automatically builds and deploys to
    [the production](https://www.matedansleretro.fr) on each push on `prod`
11. Conduct one last final check of your changes on [the production](https://www.matedansleretro.fr)
12. Backmerge the `prod` branch to `main`:
    `git checkout main && git pull && git merge origin/prod`

> **Always backmerge `prod` to `main`** to keep branches synchronized.

#### Fast workflow

If you know what you are doing, you can skip the whole "new branch and PR to
`main`" part to directly commit and push to the `main` branch:

1. Write your code and push it to directly to the `main` branch
2. Vercel automatically builds and deploys the `main` branch to
   [the preprod environment](http://preview.matedansleretro.fr/) on each push on
   `main`
3. Check your changes on [the preprod](http://preview.matedansleretro.fr/)
4. Once tested and approved, create a PR from `main` into `prod` and merge it
   **(using merge commit)**

> You could also manually merge `main` into `prod` using Git:
> `git checkout prod && git pull && git merge origin/main && git push`
> Note though that
> **creating a PR is recommended to have proper history and traceability**

5. Vercel automatically builds and deploys to
   [the production](https://www.matedansleretro.fr) on each push on `prod`
6. Conduct one last final check of your changes on [the production](https://www.matedansleretro.fr)
7. Backmerge the `prod` branch to `main`:
   `git checkout main && git pull && git merge origin/prod`

> **Always backmerge `prod` to `main`** to keep branches synchronized.

#### Hotfix

If you need to make urgent fixes directly to production:

1. Create a new branch from `prod`:
   `git checkout prod && git pull && git checkout -b hotfix/my-branch`
2. Write your code and push it to your branch
3. Create a PR to `prod`
4. Vercel automatically builds and deploys your PR on a dedicated environment
   _(URL will be available in your PR)_ on each push
5. Check your changes in this dedicated environment
6. Once tested and approved, merge your PR into `prod` **(using squash commit)**
7. Vercel automatically builds and deploys the `prod` branch to
   [the prod environment](http://www.matedansleretro.fr/) on each push on
   `prod`
8. Check your changes on [the prod](http://www.matedansleretro.fr/)
9. Backmerge the `prod` branch to `main`:
   `git checkout main && git pull && git merge origin/prod`

> **⚠️ Important**: Hotfixes should only be used for critical issues that cannot
> wait for the normal workflow.

> **Always backmerge `prod` to `main`** to keep branches synchronized.

#### Fast Hotfix

To deploy hotfixes to production even faster:

1. Write your code and push it directly to the `prod` branch
2. Vercel automatically builds and deploys the `prod` branch to
   [the prod environment](http://www.matedansleretro.fr/) on each push on
   `prod`
3. Check your changes on [the prod](http://www.matedansleretro.fr/)
4. Backmerge the `prod` branch to `main`:
   `git checkout main && git pull && git merge origin/prod`

> **⚠️ Important**: Hotfixes should only be used for critical issues that cannot
> wait for the normal workflow.

> **Always backmerge `prod` to `main`** to keep branches synchronized.

### Manual Deployment

If you need to deploy elsewhere than Vercel:

1. **Build**: No build step required - files are ready to serve
2. **Deploy**: Upload all files to any static hosting service
3. **Configure**: Ensure `index.html` is set as the entry point

## License

This project is the official website of Mate Dans Le Rétro... Gaming association.
