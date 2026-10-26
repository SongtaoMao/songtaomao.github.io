# Website Management Setup — 2026-10-26

This round establishes ongoing website maintenance. Website source and hosting settings are unchanged.

- Created a dedicated management checkout in the current workspace from the clean existing repository; retained the earlier checkout as a historical copy.
- Added repository instructions and a maintenance guide covering file locations, preview branches, publication, temporary pause/restore, and round-by-round result recording.
- Preserved the preview-before-publication preference for visible website changes.
- Corrected the operational baseline: the last content release was `21002e1d09787c1a5ab756552f195a078958190b`, published on 2026-10-13 (America/Los_Angeles), with Pages run #27 successful. The older result below retains its original date and run #18 reference as historical text.

Validation performed before syncing these documentation changes:

- GitHub main and both local copies initially matched `21002e1`; both local workspaces were clean.
- GitHub Pages API: `status=built`, `build_type=legacy`, source `main /`, no custom domain, HTTPS enforced.
- The public homepage returned HTTP 200.
- Downloaded homepage and local `index.html` had identical SHA-256: `d20f11b7ae18ab5eef8727aca219187882562344a9cd2cf377aa9ab6d963a300`.
- The Pages run for that content release was successful: https://github.com/SongtaoMao/songtaomao.github.io/actions/runs/38444203819.
- Only management documentation and ignore rules are included in this setup; no heavy jobs were run.
- Search Console's current indexing/sitemap processing state was not checked. Earlier indexing observations below are historical.
- No Overleaf remote is configured for this website.

The setup commit may trigger another Pages deployment with unchanged homepage content. Check the corresponding Actions run when confirming deployment; the run #27 result above verifies the prior content release.

---

# Website Refresh Result

Date: 2026-10-14

- Published the updated biography with the Summer 2025 UIUC visit hosted by Fernando Granha Jeronimo, the Summer 2026 Bocconi visit hosted by Alon Rosen, and the ongoing Fall 2026 Simons Institute program on Pseudorandomness & High-Dimensional Expansion.
- Refined the introduction layout by slightly reducing its text size, combining the biography and visiting history, reducing the inter-paragraph gap, lowering the portrait by 36 pixels, and raising the email-and-icons block by 24 pixels on desktop.
- Verified the `https://songtaomao.github.io/` Search Console property via the published HTML tag. Google's live URL test reports that the page is available and indexable, and the homepage was added to Google's priority crawl queue. The prior Google index record showed a September 28, 2026 crawl that received a 404.
- Submitted `https://songtaomao.github.io/sitemap.xml` to Search Console. Its first processing status was “Sitemap could not be read,” although direct Googlebot-style access returns HTTP 200 with `application/xml`, so it may need processing time after the newly created property.
- Added the Google Search Console HTML verification tag so the restored homepage can be verified and submitted for reindexing.
- Added a canonical URL, search description, crawl-permitting `robots.txt`, and a homepage `sitemap.xml` to help Google rediscover the restored site.
- SEO indexing audit: Google currently shows no indexed result for `site:songtaomao.github.io`, while the restored homepage returns HTTP 200 with no `noindex` directive. The likely cause is deindexing during the roughly 49-day disabled/`noindex` period; a Search Console indexing request and sitemap can speed rediscovery.
- Darkened the low-degree contribution note and matched its font weight to the bold “Songtao Mao” author styling (`600`) while preserving the note's size and spacing.
- Restored the reviewed homepage for publication at https://songtaomao.github.io.
- Bolded the author-order note while preserving its existing font size and spacing.
- Clarified that the postdoctoral and research-position search starts in 2027.
- Simplified the low-degree contribution note and linked it directly to Samuel Hopkins's thesis PDF.
- Marked the PASCAL author list as ordered by contribution.
- Added a precise contribution note for the polynomial-time low-degree paper, linking to Hopkins's original 2018 thesis.
- Moved “Abelian Cayley High-Dimensional Expanders with Polylogarithmic Degree” to the top of the publication list.
- Added the five publications missing from the previous homepage, bringing the list to 12 entries.
- Marked the planted-clique paper as SODA 2027 and the Batch LPN paper as TCC 2026.
- Updated PASCAL to its latest title and author list.
- Corrected the author order and venue year for the Nilpotent Category paper.
- Added a homepage note inviting contact about postdoctoral and other research positions.
- Restored the repository name to `songtaomao.github.io` and published from `main / (root)`.

Validation completed:

- HTML parsed successfully.
- All 12 publication entries are present.
- Git whitespace validation passed.
- GitHub Pages deployment run #18 completed successfully.
- The public site returned HTTP 200 and the live content was independently verified.
