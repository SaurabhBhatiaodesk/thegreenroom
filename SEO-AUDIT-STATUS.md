# SEO audit follow-up

Changes are local theme changes. Live deployment, a full storefront preview, and a new crawl have not been performed. Do not report the original audit counts as resolved counts.

## Theme changes

- Main product titles use H1; featured products retain H2.
- First supported page/blog hero headings use H1. Templates without a primary heading receive an accessible, visually hidden H1 without adding a visible row.
- Blog index cards use H2. Decorative overlines, button labels, and prose no longer use heading tags. Repeated and initially empty theme headings have been corrected.
- Heading styling is retained through existing classes and data attributes. The wedding paragraph's original bold styling is preserved separately from its tag.
- Product, card, article, collection, and logo images use saved alt text first and contextual titles where available. Decorative images may correctly retain empty alt text.
- Shared image requests are capped at the existing responsive image limits (3000px desktop, 1600px mobile). Two custom section images use sizes appropriate to their existing CSS display dimensions.
- Product card, mini-card, gallery, modal, and thumbnail image requests are capped at their existing responsive image limits. The higher-resolution zoom image remains available.
- Existing intrinsic image width/height attributes are retained explicitly while changing request sizes, preserving layout geometry.
- Custom banner images have intrinsic width/height attributes. Pickup section schema has a valid name.
- Social image URLs use HTTPS. Social text is HTML-escaped once.
- Product structured data uses JSON-safe text values and string GTINs. Article schema uses Shopify's structured_data filter. Other page types receive WebPage, CollectionPage, Blog, or WebSite structured data.

## Shopify Admin / content work still needed

- Client: SEO title and metafield edits; confirm ownership of meta descriptions.
- Broken links in blog content: verify each replacement destination, then update source article content. External destinations must not be guessed.
- Messy/long product and article handles: choose final handles and create redirects for old URLs in Shopify Admin.
- Oversized images embedded directly in blog/page rich text: replace with appropriately sized assets or content image URLs.
- Product images smaller than 500x500: upload higher-resolution originals. A theme cannot recover missing image detail.
- Missing descriptive alt text on content images: supply accurate descriptions in Shopify Admin. Contextual fallback text is not a substitute for describing every image.
- Orphan pages and thin content: review which pages should remain published; add relevant content and intentional navigation links.
- Multiple/empty headings inside stored blog/page content require source-content edits.

## Existing theme issue outside the audit fixes

sections/mh_parallax_banner.liquid references the missing snippets/Sign_Up.liquid when a SignUp block is configured. Its intended design is absent from this checkout, so it has not been recreated from guesswork.

## Verification

- Earlier heading changes: 32 desktop/mobile component style comparisons matched the original styles.
- Image layout changes: 10 comparisons at 1440px and 390px matched the original image bounding boxes.
- Shopify validation is run on each changed file. Pre-existing warnings are distinguished from new findings.

Source: site-audit-ad6e436a-7f3f-4b73-9e25-1e7fa5354052 (1).xlsx, crawl completed 13 October 2026.
