# Product recommendation standards

Every product recommended on Budget Living 4 All must meet these criteria before it goes in an article.

## Minimum requirements
- At least 1,000 Amazon reviews
- 4.0 stars or higher
- Currently in stock and available to ship
- Price verified at time of writing

## What to include in every product box
- Star rating (e.g. "4.6 stars")
- Review count (e.g. "19,959+ Amazon reviews")
- Honest summary of what reviewers commonly praise
- Honest summary of any common complaints — do not hide these
- Affiliate link with tag: budgetliving4-20
- Date rating/count was checked (add to article sources footnote)

## Affiliate link format
```
https://www.amazon.com/dp/[ASIN]?tag=budgetliving4-20
```

## Product box HTML template
```html
<div class="product-box">
  <img src="/assets/images/[image-filename].jpg" alt="[descriptive alt text]" />
  <div class="product-info">
    <h4>[Product name]</h4>
    <p>[X] stars · [N]+ Amazon reviews. [2-3 sentences: what it does, what reviewers praise, any honest caveats worth knowing.]</p>
    <a href="https://www.amazon.com/dp/[ASIN]?tag=budgetliving4-20" class="btn-affiliate" rel="nofollow sponsored" target="_blank">Check price on Amazon</a>
  </div>
</div>
```

## Sources footnote addition (add to every article with product links)
```
· Product ratings and review counts sourced from Amazon.com as of [Month Year].
```

## Products verified so far

| Product | ASIN | Stars | Reviews | Verified |
|---------|------|-------|---------|----------|
| Pyrex Simply Store 18-Piece Glass Storage Set | B0157G34AY | 4.6 | 19,959+ | June 2025 |
| ThermoPro TP03 Digital Instant Read Thermometer | B01IHHLB3W | 4.7 | 50,000+ | June 2025 |

## Getting the product image

Amazon does not allow hotlinking their product images. To get the image for a product box:

1. Go to the product's Amazon page
2. Right-click the main product image and save it
3. Name it clearly: e.g. `pyrex-simply-store.jpg`
4. Save it to `assets/images/` in the repo
5. Reference it in the product box as `{{ '/assets/images/filename.jpg' | relative_url }}`

This is permitted under Amazon's affiliate program terms for the purpose of promoting products you are linking to.

## Process for each new article
1. Search Amazon for the product category
2. Filter by 4+ stars, sort by review count
3. Cross-reference against independent review sites (not sponsored content)
4. Note any common complaints from reviews and include them honestly
5. Record ASIN, star rating, review count, and date checked
6. Add to the table above
