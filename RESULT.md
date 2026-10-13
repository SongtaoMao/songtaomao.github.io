# Website Refresh Result

Date: 2026-10-13

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
