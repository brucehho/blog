---
description: how to publish a new blog post
---

## Steps

1. Create or edit the required markdown files in `_posts/`
2. Verify front matter is correct (title, date, lang, slug, permalink, categories, tags, summary, toc)
   - Chinese (`.md`): permalink `/category/slug/`
   - English (`.en.md`): permalink `/category/slug-en/`
   - Japanese (`.ja.md`): permalink `/category/slug-ja/`
3. Review content for accuracy

// turbo
4. Stage, commit and push all changes to GitHub:
```
git add -A && git commit -m "<descriptive message>" && git push origin main
```
