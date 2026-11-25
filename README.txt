Momentz deploy handoff
======================

The live site (https://www.momentz.ventures/) is a static HTML site hosted on Vercel.
https://momentz.ventures/ already 307-redirects to the www host.
There is no Webflow / Framer / WordPress / Wix layer. Root files such as
robots.txt, sitemap.xml and llms.txt can be placed in the project root and
will be served at the site root. That is not possible on Webflow without a
workaround; it is native on Vercel.

A) To add LLM/SEO files to the CURRENT live site (keep today's design)
   1. In the existing Vercel project, add these files at the root (same level as the current index.html):
        robots.txt
        sitemap.xml
        llms.txt
        llms-full.txt
        og-image.png   (already live at /og-image.png; included here for completeness)
   2. Optionally paste schema-and-meta.html into the current homepage <head>
      (the live site already has OG tags and JSON-LD; this snippet is a
      tighter, docs-safe version).
   3. Redeploy. No platform “backend” or CMS to update.

B) To replace the live site with the v16 prototype (new design)
   Upload this whole folder as the Vercel project root, or set index.html
   as the output. index.html is the packaged v16 single file (HTML + CSS + JS
   + assets inlined). Then add the same root files as in A (already in this
   folder). This is a visual redesign — review it before going to production.

Do not upload index-v14.html / app-v14.js without their image and font
dependencies; the packaged index.html in this folder is the file meant for
a quick Vercel upload.

This drop is v16: harmonic plate motion, a 75s anti-clockwise orbit of the
satellite constellations (center stays), and gentle pointer-velocity parallax
on desktop and iPad. Phone layout (max-width 768px) is unchanged from v15.
