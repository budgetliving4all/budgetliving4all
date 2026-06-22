# Budget Living 4 All — Jekyll Site

## Deploy to your existing GitHub repo

This replaces the contents of `budgetliving4all/budgetmealprep`.

### Option 1: Upload via GitHub web UI (easiest)
1. Go to github.com/budgetliving4all/budgetmealprep
2. Delete old files you're replacing (or just overwrite)
3. Drag and drop all files from this zip into the repo
4. Commit — site rebuilds in ~2 minutes

### Option 2: Git (if you have it set up locally)
```bash
# In your local clone of the repo:
cp -r /path/to/this/zip/* .
git add .
git commit -m "Rebrand to Budget Living 4 All"
git push
```

---

## Writing a new article

1. Copy `_posts/TEMPLATE-article.md`
2. Rename: `YYYY-MM-DD-your-slug.md`
3. Fill in the front matter
4. Write the article
5. Push to GitHub — live in 2 minutes

## Article checklist
- [ ] Target keyword in title and first paragraph
- [ ] Meta description 140-155 characters
- [ ] `quick_answer` filled in
- [ ] 2+ internal links to other articles
- [ ] `affiliate_disclaimer: true` if affiliate links used
- [ ] `read_time` estimated

## Site structure
```
budgetliving4all/
├── _config.yml           Main config — update url/baseurl if adding custom domain
├── _layouts/             Page templates
├── _includes/            Header, footer, sidebar, related posts
├── _posts/               Articles go here (YYYY-MM-DD-slug.md)
├── assets/css/main.css   All styles
├── index.md              Homepage
├── meal-prep.md          /meal-prep/ category page
├── budget-tips.md        /budget-tips/ category page
├── reviews.md            /reviews/ category page
├── about.md              /about/
├── privacy.md            /privacy/
├── affiliate-disclosure.md
└── contact.md

```

## Adding a new site section
1. Create a new category page (e.g. `frugal-living.md`) following the pattern in `meal-prep.md`
2. Add a nav link in `_includes/header.html`
3. Use the new category name in article front matter: `categories: [frugal-living]`

## Switching to a custom domain later
1. Buy domain at Namecheap or Cloudflare (~$12/yr)
2. In `_config.yml`: change `url` to your domain, change `baseurl` to `""`
3. In GitHub repo Settings > Pages > Custom domain: enter your domain
4. Add DNS records at your registrar:
   ```
   A  @  185.199.108.153
   A  @  185.199.109.153
   A  @  185.199.110.153
   A  @  185.199.111.153
   CNAME  www  budgetliving4all.github.io
   ```

## Amazon Associates
1. Sign up: affiliate-program.amazon.com
2. Get your tag (e.g. `budgetliving4all-20`)
3. Replace `YOUR-AFFILIATE-TAG` in product links
4. Set `affiliate_disclaimer: true` in any article with affiliate links

## Contact
budgetliving4all@gmail.com
